# Concept proposals for a better operating system

Here I list the various ideas and concepts which I have collected into what I
consider to be the necessary operating system to subsane the current security
and productivity flaws on modern operating systems' design and implementation.

This list is preliminary, Q&D and subject to debate, as it is intended to be a
catalysis for the creation of new projects that address today's problems, and
not a mere exercise of brainstorming for the sake of ego and fun (right?). All
of the ideas shown below have not been put into strict thought, and it has not
been considered deeply whenever they are wrong or in contradiction with others.
I am, after all, not an operating systems designer, and got yet to read even a
single Tanenbaum book. Sorry.

Please help by contributing to this list and debating about its virtues and
failures, as well as completing and extending it, and considering its potential
appliance into the real, desperate world ruled by vulnerable Windows and Linux
installations that can't stop breaking and DDoSing stuff because it's so cool.
Hopefully you may even manage to make it formal and presentable!

## Proposed ideas

- Microkernel (modular) with an integrated virtual machine
	- To heavily consider: JVM, V8, Servo
		- Java bytecode or WebAssembly?
	- Designed for 64 and 128 bits processors from the start
- Native isolation via virtual machine
	- Compatible with AOT compilation
	- Probably also LXC-style containers?
- Kernel / virtual machine programmed on Rust
	- Systems language with high-level abstractions
	- Designed to meet the current and future needs
	- Warranty against memory races and segfaults (**essential**)
	- Already targets all of Intel and ARM processors
	- It's already perfect and no other language can be an improvement
		- Biased? Meh, who cares.
- Permissions layer integrated along with VM isolation
- Authentication system via system-level cryptography
	- Probably PGP being the best choice
		- PGP is the Major Key to Success!™
		- Should allow switching to any other trustable system
	- For storing data
	- For signing binaries, repositories, drivers, etc.
	- For identifying people, including contacts
	- For protecting sent information
- Native support for multiple programming languages
- Virtualization support
	- Via containers?
	- Should also be designed to be *contained*
- Net-distributed resource management
	- Device management *a la Plan 9 / Hurd*
	- Own filesystem
		- Non-hierarchical, if possible
		- Organized by metadata, *a la BeFS*
		- Search-oriented
			- Could replace Google in a future!
		- With edition history *a la Git / Nix*
		- Distributed
	- Support for other distributed filesystems, such as IPFS
	- Multiple origins' software management
		- Allows making changes depending on available permissons *a la Nix*
		- Integration with metadata filesystems 
			- In order to better organize the userland
		- Integration with distributed filesystems
			- In order to better support third-party repositories
			- In order to support network-shared software (intranet)
		- Support for package scripts
			- Support for a community-driven repository *a la AUR*
				- *"If it's not at the AUR, it doesn't exist!"*
- Dynamic user interface
	- Without a default, kernel-level way of interacting
	- Preferably a graphical server, even for text input
		- Instead of SSH, a graphical terminal session (?)
			- No need to make it this way, just saying (???)
	- Out-of-the-box 3D support
		- Vulkan would be great - imagine this thing on game consoles!
	- Out-of-the-box support for touch input
		- Modular, capable of adapting to currently non-invented input methods
	- "Convergent", adaptable to the device in which is being used
	- Workflow based in transactions that do transformations
		- Functional programming would be essential
			- (statement ((for (verbose (lisp (parenthesis))) (no (need))) (tho)))
				- *(Not personally against them. But some people are.)*
	- User applications integrated into the user interface
		- Hope this could be possible without sacrificing any portability
	- Integrated support for running remote applications	

## Design influences

While making this list, I was inspired by the following awesome tech. Thank you all
for helping to make the world a better place!

- **Rust**, **Go** and **D**, for opening the path towards new, safer software. 
- **Java** and **JavaScript**, for introducing virtual machines into our daily lifes.
- **Plan 9**, **Minix** and **GNU Hurd**, for teaching us that microkernel-based, distributed systems are lit.
- **IPFS** and **ZeroNet**, for teaching us that distributed networks are lit.
- **BeOS** and its son **Haiku**, for showing us there's life beyond hierarchical filesystems.
- **PGP** and **Bitcoin**, for giving control back to people.
- **Git**, **Étoilé** and **Nix**, for so many bytes of data that have been and will be rescued.
	- Git is lit, indeed.
	- Also please check out [Étoilé](http://etoileos.com), really nice project!
- **Lisp**, **Haskell** and **Guix**, for teaching me the goods of functional programming.
- **Pacman** and the **Arch User Repository**, for rocking so much.

