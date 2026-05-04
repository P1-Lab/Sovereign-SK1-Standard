# Specification: Memory Topology (The TapRoot & The Scar)

## 1. L0 Registry: The TapRoot
* **Type**: Non-volatile, read-only hardware block (64K SRAM/Gate Array).
* **Function**: Serves as the vitrified "Soul-State." It contains the immutable logic constants that define the machine’s core behavior and identity.
* **Access**: Hardware-locked at the bus level; cannot be modified by L2 volatile workspace or external I/O.

## 2. L1 Accretion Layer: The Scar
* **Type**: High-durability write-once/read-many (WORM) storage.
* **Function**: Captures transient data as irreversible accretion. This layer prevents "context decay" by treating memory as a permanent physical change to the state-lattice rather than a sliding window.

## 3. L2 Volatile Workspace
* **Type**: Standard high-speed RAM.
* **Function**: Temporary signal buffer for real-time processing. Data in L2 is flushed every power cycle and never influences the L0 TapRoot constants.
