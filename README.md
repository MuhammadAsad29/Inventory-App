# Inventory App — Swing-based Inventory Management System

A desktop Inventory Management application built with Java Swing.  
It provides a graphical user interface (GUI) for adding, updating, deleting, searching, saving, and loading inventory items (stored as simple CSV lines in a local file).

---

## Project summary

**Main source file:** `INVENTORY MANAGEMENT SYSTEM/src/InventoryItem.java`

This file contains two classes:
- `InventoryItem` — model class representing an item (id, name, quantity, price) and includes `toString()` that formats the item as CSV.
- `InventoryApp` — a `JFrame`-based Swing application that provides the GUI and application logic (table display, add/update/delete, search, save/load to `inventory.txt`). The `main()` method is in `InventoryApp` and launches the GUI.

**Key features implemented:**
- Graphical UI using Java Swing (`JFrame`, `JTable`, `JButton`, `JTextField`, `JOptionPane`).
- Tabular inventory display backed by `DefaultTableModel` and `TableRowSorter` for search/filtering.
- Add new items and update existing items (identified by ID).
- Delete selected items from the table and internal `ArrayList<InventoryItem>`.
- Save inventory to `inventory.txt` (CSV format via `toString()` lines).
- Load inventory from `inventory.txt` and populate the table.
- Basic input validation and user feedback dialogs (success/error).

**Notes about the source layout:** No Java package is declared; both classes are defined inside a single `.java` file (`InventoryItem.java`). The project was likely created in an IDE (Swing UI developed in IntelliJ), and no external libraries are required — only the Java Standard Library (AWT/Swing, IO, util).

---

## How to compile and run (command-line)
1. Ensure JDK 20+ is installed and `javac`/`java` are on your `PATH`.
2. Open a terminal and navigate to the folder that contains the `src` directory:

```bash
cd "INVENTORY MANAGEMENT SYSTEM/src"
```

3. Compile the Java source (this will produce `.class` files for both classes):

```bash
javac InventoryItem.java
```

4. Run the application (the `main` method is in `InventoryApp`):

```bash
java InventoryApp
```

On launch, a window appears with fields for ID, Name, Quantity, Price, a table view of items, and buttons for Add/Update/Delete/Save/Load/Search/Clear.

> Alternative: Import the project into IntelliJ IDEA or Eclipse and run the `InventoryApp` class from the IDE (recommended for easier debugging and editing).

---

## Files included (from the uploaded archive)
- `INVENTORY MANAGEMENT SYSTEM/src/InventoryItem.java` — main source file (contains `InventoryItem` and `InventoryApp`).
- (The archive may also include IDE metadata; the core runnable artifact is the `src` file above.)

---

## Suggestions & possible improvements
- **Separate classes into files** and declare a package (e.g., `com.yourname.inventory`) for clearer structure and easier maintenance.
- **Add input validation** to prevent duplicate IDs and improve numeric parsing error messages.
- **Improve persistence**: support CSV with header, or use JSON, and allow custom file selection with a file chooser (`JFileChooser`).
- **Add unit tests** (JUnit) for inventory logic separated from UI code.
- **Create a build file** (`pom.xml` for Maven or `build.gradle` for Gradle) to enable reproducible builds and packaging (fat JAR).
- **Export as runnable JAR** so users can launch the GUI by double-clicking (or `java -jar app.jar`).

---

## License & Author
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Author: Muhammad Asad


---

If you want, I can now:
- Split the single `.java` file into separate files and add a package structure.
- Create a `.gitignore` tuned for IntelliJ + Java and remove compiled artifacts from the archive.
- Generate a `pom.xml` or `build.gradle` for easy building and a script to create a runnable JAR.

