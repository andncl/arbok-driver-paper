# Letter to the Editor – SoftwareX

Dear Editors,

We would like you to consider our submission – *"arbok-driver: A modular and parameterized Python framework for FPGA-based quantum measurement routines"* – for publication in SoftwareX.

## Background

FPGA-based arbitrary waveform generators are central to the control and readout of qubit experiments, enabling deterministic, low-latency execution of complex pulse sequences. Although most instrument manufacturers provide high-level abstraction layers, developing scalable and maintainable measurement routines remains difficult in practice due to deeply nested logic, large numbers of interdependent parameters, and the need to coordinate hardware-level timing with higher-level experimental workflows. As qubit systems scale from few-qubit demonstrations toward arrays of tens to hundreds of qubits, the lack of flexible and reproducible measurement software becomes a critical bottleneck.

## Main contribution

Our manuscript presents arbok-driver, an open-source Python package that dynamically generates a fully parameterized instrument interface for FPGA-based quantum measurements. Rather than requiring users to write or maintain low-level FPGA code, arbok-driver constructs executable hardware programs from modular, composable Python building blocks and device-specific configurations. All relevant pulse sequence parameters are automatically exposed through the QCoDeS instrumentation framework, enabling seamless integration with existing laboratory infrastructure.

The framework fundamentally changes the workflow of experimentalists: the role shifts from hardware programmer to measurement designer, where the focus is on defining the physics of the experiment rather than managing timing constraints and register-level details. New users can begin acquiring data within minutes by reusing existing sequence components, and measurements are guaranteed to execute identically regardless of which setup or operator runs them.

## Scientific impact

arbok-driver has directly contributed to two recent high-impact publications. It supported the tuning and coherent control of an eight-qubit linear array fabricated in a 300 mm CMOS-compatible foundry process, the largest number of individually controlled silicon SiMOS spin qubits reported to date in an industrially fabricated platform (Nickl et al., *Nature Communications*, 2025; accepted with editorial revisions). It also enabled device pre-screening from the same foundry process, contributing to the demonstration of single- and two-qubit gate fidelities exceeding 99% (Steinacker et al., *Nature* **646**, 81–87, 2025). These results demonstrate that flexible, reproducible control software is a prerequisite for translating high-fidelity qubit performance from academic settings to industry-compatible fabrication processes.

## Adoption and reusability

The framework has been adopted at Diraq, a silicon quantum computing startup, where it is currently deployed across six independent measurement campaigns spanning mass device characterisation, qubit array scale-up, qubit benchmarking, novel qubit architectures (singlet-triplet/ exchange only), and automated tuning with machine learning protocols. The package is open-source (MIT license), installable via standard Python tooling, and includes comprehensive documentation with tutorials. Currently implemented for the Quantum Machines OPX platform, the underlying design principles of modular sequence composition, dynamic parameter exposure, and device-agnostic configuration are transferable to other FPGA backends. Notably, research groups and companies across the quantum computing community face the same challenge of building and maintaining custom measurement codebases, often duplicating significant engineering effort independently. By providing a reusable, well-documented framework, arbok-driver reduces this redundancy and offers a foundation that others can adopt or extend rather than rebuilding from scratch.

## Relevance to SoftwareX

We believe this manuscript is well suited to SoftwareX because it describes a reusable, open-source research tool with demonstrated scientific impact, broad community relevance, and clear documentation. The software addresses a practical challenge faced by a growing number of experimental groups working with FPGA-based quantum control systems, and its design principles are transferable across qubit platforms.

## Suggested reviewers

1. **Julian M. Bopp**, Humboldt-Universität zu Berlin, Germany
   First author of DynExp, a Python-based laboratory automation framework for dynamically changing quantum experiments. Directly familiar with the challenges of building modular experiment automation software.

2. **Rodolfo Carobene**, Università Milano Bicocca, Italy
   Lead developer of Qibosoq, an open-source Python framework for quantum circuit programming on RFSoC FPGAs. Has hands-on experience building the same class of abstraction layer over FPGA hardware.

3. **Sara Sussman**, Fermi National Accelerator Laboratory, USA
   PhD thesis on open-source qubit control software (QICK). Understands the challenges of building reusable quantum measurement frameworks from both a developer and user perspective.

4. **Andrea Pasquale**, University of Milan, Italy
   First author of Qibocal, open-source software for characterization and calibration of quantum processors. Experienced with the full measurement stack from hardware drivers to automated calibration routines.

---

Thank you, in advance, for your consideration of our manuscript.

Yours sincerely,

Andreas Nickl, Tuomo Tanttu
(on behalf of all co-authors)

School of Electrical Engineering & Telecommunications,
UNSW Sydney, NSW 2052, Australia

Email: a.nickl@unsw.edu.au, t.tanttu@unsw.edu.au
