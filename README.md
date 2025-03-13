Fun-AI mainchain
=====================================

What is FUN-AI mainchain?
---------------------

The FUN-AI Mainchain plays a crucial role in the FUN-AI ecosystem, acting as the primary settlement layer for AI-generated content (AIGC) task computation. Its key responsibilities include:


1. Settlement Layer for AI Task Computation
	•	The Mainchain records AI task execution states and computation results, ensuring transparency and verifiability.
	•	Tasks such as publishing, executing, and confirming AI-generated results are settled on the Mainchain.

2. Ensuring Computational Integrity
	•	On-chain task records: Execution hashes, computing node identities, and timestamps are stored on-chain, ensuring immutability.
	•	Result validation: Computation results submitted by nodes undergo consensus verification, preventing fraud or manipulation.
	•	Preventing double spending: The Mainchain enforces unique reward distribution through its consensus mechanism.

3. Token Economy and Incentive Mechanism
	•	Rewarding computing nodes: Nodes that contribute computational resources receive FUN tokens on the Mainchain.
	•	Token issuance and management: The Mainchain governs the issuance, distribution, and transaction settlement of FUN-AI tokens.
	•	Staking and governance: Advanced tasks may require nodes to stake tokens to prevent malicious activity, and the Mainchain supports governance through community voting.

4. Task Scheduling and Resource Coordination
	•	The Mainchain facilitates the matching of AI tasks with suitable computing nodes.
	•	It ensures efficient allocation of computing resources based on demand and supply.
	•	Computation results are securely stored and referenced, ensuring data consistency.

5. Security Anchoring with Bitcoin
	•	Potential integration with Bitcoin for security anchoring, leveraging Bitcoin’s immutability to store AI task proofs.
	•	Similar to the Stacks model, the FUN-AI Mainchain may use Bitcoin anchoring to enhance security and prevent tampering.

6. Smart Contract Support for AI Computation
	•	The Mainchain may support Clarity or EVM-compatible smart contracts, enabling:
	•	Automated AI task execution rules.
	•	Payment and validation mechanisms for AI computations.
	•	DeFi-like economic models for task bidding, computing power leasing, and reward distribution.

Conclusion

The FUN-AI Mainchain serves as the settlement layer, security framework, incentive hub, and task coordination system for AI task computation. It ensures trustworthy execution, decentralized governance, and efficient resource allocation, potentially anchoring to Bitcoin for enhanced security and reliability.

License
-------

FUN-AI mainchain is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built (see `doc/build-*.md` for instructions) and tested, but it is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly from release branches to indicate new official, stable release versions of Bitcoin Core.

The https://github.com/bitcoin-core/gui repository is used exclusively for the
development of the GUI. Its master branch is identical in all monotree
repositories. Release branches and tags do not exist, so please do not fork
that repository unless it is for development reasons.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled during the generation of the build system) with: `ctest`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python.
These tests can be run (if the [test dependencies](/test) are installed) with: `build/test/functional/test_runner.py`
(assuming `build` is your build directory).

The CI (Continuous Integration) systems make sure that every pull request is built for Windows, Linux, and macOS,
and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://www.transifex.com/bitcoin/bitcoin/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.
