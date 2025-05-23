<!DOCTYPE html>
<html>
<head>
    <title>Bit Replacement Entry Form</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
        }
 
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 20px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
 
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
            padding: 30px;
        }
 
        h2 {
            color: var(--primary);
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 30px;
        }
 
        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
 
        .form-group {
            position: relative;
        }
 
        label {
            display: block;
            margin-bottom: 8px;
            color: var(--primary);
            font-weight: 500;
        }
 
        input, select {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            transition: all 0.3s ease;
        }
 
        input:focus, select:focus {
            border-color: var(--secondary);
            outline: none;
            box-shadow: 0 0 8px rgba(52, 152, 219, 0.3);
        }
 
        input[readonly] {
            background-color: #f8f9fa;
            cursor: not-allowed;
        }
 
        .button-group {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin-top: 25px;
        }
 
        button {
            padding: 12px 25px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
 
        button.primary {
            background: var(--secondary);
            color: white;
        }
 
        button.success {
            background: #27ae60;
            color: white;
        }
 
        button.danger {
            background: var(--accent);
            color: white;
        }
 
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <div class="container">
        <h2><i class="fas fa-tools"></i> Bit Replacement Entry Form</h2>
        
        <form id="dataForm">
            <div class="form-grid">
                <!-- Auto-generated Date/Time -->
                <div class="form-group">
                    <label><i class="fas fa-calendar-day"></i> Date</label>
                    <input type="date" name="date" id="autoDate" readonly>
                </div>
                
                <div class="form-group">
                    <label><i class="fas fa-clock"></i> Time</label>
                    <input type="time" name="time" id="autoTime" readonly>
                </div>
 
                <!-- User Input Fields -->
                <div class="form-group">
                    <label><i class="fas fa-hashtag"></i> Part No</label>
                    <input type="text" name="partNo" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-cog"></i> Bit Type</label>
                    <select name="bitType" id="bitType" required>
                        <option value="">-- Select Bit Type --</option>
                        <option value="POINT BIT">POINT BIT</option>
                        <option value="FLAT BIT">FLAT BIT</option>
                        <option value="ANGLE BIT">ANGLE BIT</option>
                    </select>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-ruler"></i> Bit Size</label>
                    <input type="text" name="bitSize" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-cubes"></i> Bit Quantity</label>
                    <input type="number" name="bitQuantity" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-exclamation-triangle"></i> Replacement Reason</label>
                    <input type="text" name="replacementReason" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-thermometer-quarter"></i> Old Tip Temperature</label>
                    <input type="text" name="oldTipTemperature" required>
                </div>

                <div class="form-group">
                    <label><i class="fas fa-thermometer-three-quarters"></i> New Tip Temperature</label>
                    <input type="text" name="newTipTemperature" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-project-diagram"></i> Line No</label>
                    <input type="text" name="lineNo" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-layer-group"></i> Stage No</label>
                    <input type="text" name="stageNo" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-file-alt"></i> IS No</label>
                    <input type="text" name="isNo" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-user-tie"></i> Supervisor Name</label>
                    <input type="text" name="supervisorName" id="supervisorName" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-id-card"></i> Supervisor Employee No</label>
                    <input type="text" name="supervisorEmpNo" id="supervisorEmpNo" required>
                </div>
 
                <div class="form-group">
                    <label><i class="fas fa-user-check"></i> Given By</label>
                    <input type="text" name="givenBy" required>
                </div>
            </div>
 
            <div class="button-group">
                <button type="submit" class="primary">
                    <i class="fas fa-save"></i> Submit Entry
                </button>
                <button type="button" id="resetFormBtn" class="danger">
                    <i class="fas fa-undo"></i> Reset Form
                </button>
                <button type="button" id="downloadCsvBtn" class="success">
                    <i class="fas fa-download"></i> Download All as CSV
                </button>
                <button type="button" id="clearEntriesBtn" class="warning" style="background-color: #f39c12;">
                    <i class="fas fa-trash-alt"></i> Clear All Entries
                </button>
                <button type="button" id="loadDataBtn" class="info" style="background-color: #17a2b8;">
                    <i class="fas fa-upload"></i> Load Data from CSV
                </button>
            </div>
        </form>

        <input type="file" id="csvFileInput" accept=".csv" style="display: none;">
        <hr style="margin: 40px 0;">

        <h3><i class="fas fa-list-alt"></i> Submitted Entries</h3>
        <div id="entriesTableContainer">
            <p id="noEntriesMessage">No entries submitted yet.</p>
            <table id="entriesTable" style="width:100%; border-collapse: collapse; display:none;">
                <thead>
                    <!-- Headers will be dynamically inserted here -->
                </thead>
                <tbody>
                    <!-- Data rows will be dynamically inserted here -->
                </tbody>
            </table>
        </div>
    </div>
 
    <script>
        // Auto-generate date and time
        function updateDateTime() {
            const now = new Date();
            document.getElementById('autoDate').value = now.toISOString().split('T')[0];
            document.getElementById('autoTime').value = now.toTimeString().slice(0,5);
        }
        updateDateTime();
        setInterval(updateDateTime, 1000);

        // Supervisor Data
        const supervisors = [
            { empNo: "47042", name: "Arun Kumar" },
            { empNo: "1002", name: "Priya Mehta" },
            { empNo: "1003", name: "Ankit Verma" },
            { empNo: "1004", name: "Neha Singh" },
            { empNo: "1005", name: "Aman Joshi" },
            { empNo: "1006", name: "Ritu Patel" },
            { empNo: "1007", name: "Sandeep Yadav" },
            { empNo: "1008", name: "Kavita Nair" },
            { empNo: "1009", name: "Mohit Bansal" },
            { empNo: "1010", name: "Swati Deshmukh" },
            { empNo: "1011", name: "Deepak Choudhary" },
            { empNo: "1012", name: "Sneha Sinha" },
            { empNo: "1013", name: "Harshad Kulkarni" },
            { empNo: "1014", name: "Isha Saxena" },
            { empNo: "1015", name: "Vinay Thakur" },
            { empNo: "1016", name: "Pooja Rawat" },
            { empNo: "1017", name: "Arjun Reddy" },
            { empNo: "1018", name: "Meena Kumari" },
            { empNo: "1019", name: "Rohit Malhotra" },
            { empNo: "1020", name: "Aarti Sharma" }
        ];

        const supervisorNameInput = document.getElementById('supervisorName');
        const supervisorEmpNoInput = document.getElementById('supervisorEmpNo');

        supervisorEmpNoInput.addEventListener('input', function() {
            const foundSupervisor = supervisors.find(s => s.empNo === this.value);
            supervisorNameInput.value = foundSupervisor ? foundSupervisor.name : '';
        });

        supervisorNameInput.addEventListener('input', function() {
            const foundSupervisor = supervisors.find(s => s.name.toLowerCase() === this.value.toLowerCase());
            supervisorEmpNoInput.value = foundSupervisor ? foundSupervisor.empNo : '';
        });

        const entriesTable = document.getElementById('entriesTable');
        const entriesTableBody = entriesTable.querySelector('tbody');
        const entriesTableHead = entriesTable.querySelector('thead');
        const noEntriesMessage = document.getElementById('noEntriesMessage');

        function displayEntries() {
            const entries = JSON.parse(localStorage.getItem('bitEntries') || '[]');
            entriesTableBody.innerHTML = ''; // Clear existing rows
            entriesTableHead.innerHTML = ''; // Clear existing headers

            if (entries.length === 0) {
                entriesTable.style.display = 'none';
                noEntriesMessage.style.display = 'block';
                return;
            }

            entriesTable.style.display = 'table';
            noEntriesMessage.style.display = 'none';

            // Create table headers from the keys of the first entry
            const headers = Object.keys(entries[0]);
            const headerRow = document.createElement('tr');
            headers.forEach(headerText => {
                const th = document.createElement('th');
                th.textContent = headerText.replace(/([A-Z])/g, ' $1').replace(/^./, str => str.toUpperCase()); // Prettify header
                th.style.border = "1px solid #ddd";
                th.style.padding = "8px";
                th.style.textAlign = "left";
                th.style.backgroundColor = "var(--light)";
                headerRow.appendChild(th);
            });
            entriesTableHead.appendChild(headerRow);

            // Populate table rows
            entries.forEach(entry => {
                const row = document.createElement('tr');
                headers.forEach(header => {
                    const cell = document.createElement('td');
                    cell.textContent = entry[header] || '';
                    cell.style.border = "1px solid #ddd";
                    cell.style.padding = "8px";
                    row.appendChild(cell);
                });
                entriesTableBody.appendChild(row);
            });
        }

        // Form handling
        document.getElementById('dataForm').addEventListener('submit', (e) => {
            e.preventDefault();
            const formData = new FormData(e.target);
            const currentEntry = {
                date: document.getElementById('autoDate').value,
                time: document.getElementById('autoTime').value,
                partNo: formData.get('partNo').toUpperCase(),
                bitType: formData.get('bitType').toUpperCase(), // Already uppercase from select, but good practice
                bitSize: formData.get('bitSize').toUpperCase(),
                bitQuantity: formData.get('bitQuantity'),
                replacementReason: formData.get('replacementReason').toUpperCase(),
                oldTipTemperature: formData.get('oldTipTemperature').toUpperCase(), 
                newTipTemperature: formData.get('newTipTemperature').toUpperCase(), 
                lineNo: formData.get('lineNo').toUpperCase(),
                stageNo: formData.get('stageNo').toUpperCase(),
                isNo: formData.get('isNo').toUpperCase(),
                supervisorName: formData.get('supervisorName').toUpperCase(), // Autofill handles case, but this ensures consistency if typed
                supervisorEmpNo: formData.get('supervisorEmpNo'), // Typically numbers or specific case, leave as is or uppercase if desired
                givenBy: formData.get('givenBy').toUpperCase()
            };
 
            // Save current entry to localStorage
            let entries = JSON.parse(localStorage.getItem('bitEntries') || '[]');
            entries.push(currentEntry);
            localStorage.setItem('bitEntries', JSON.stringify(entries));
 
            alert('Entry saved successfully to local storage!');
            e.target.reset();
            updateDateTime(); // Refresh date/time for the next entry
            displayEntries(); // Update the displayed table
        });

        // Reset button handling
        document.getElementById('resetFormBtn').addEventListener('click', function() {
            document.getElementById('dataForm').reset(); // Resets all form fields to their initial state
            updateDateTime(); // Updates the auto-generated date and time
        });

        // Clear All Entries button handling
        document.getElementById('clearEntriesBtn').addEventListener('click', function() {
            const password = prompt("Please enter the password to clear all entries:");
            const correctPassword = "secure"; // Define your password here

            if (password === null) { // User clicked Cancel or closed the prompt
                return;
            }

            if (password === correctPassword) {
                if (confirm("Are you sure you want to clear ALL submitted entries? This action cannot be undone.")) {
                    localStorage.removeItem('bitEntries');
                    displayEntries(); // Refresh the table display
                    alert('All entries have been cleared from local storage.');
                }
            } else {
                alert("Incorrect password. Entries were not cleared.");
            }
        });

        // Load Data from CSV button handling
        document.getElementById('loadDataBtn').addEventListener('click', function() {
            document.getElementById('csvFileInput').click(); // Trigger hidden file input
        });

        document.getElementById('csvFileInput').addEventListener('change', function(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const csvText = e.target.result;
                    try {
                        const loadedEntries = parseCSV(csvText);
                        if (loadedEntries.length === 0) {
                            alert("No valid entries found in the CSV file or the file is empty.");
                            return;
                        }

                        let existingEntries = JSON.parse(localStorage.getItem('bitEntries') || '[]');
                        // Simple append: You might want to add logic to prevent duplicates if needed
                        const updatedEntries = existingEntries.concat(loadedEntries);
                        
                        localStorage.setItem('bitEntries', JSON.stringify(updatedEntries));
                        displayEntries();
                        alert(`${loadedEntries.length} entries loaded successfully and appended!`);

                    } catch (error) {
                        console.error("Error parsing CSV:", error);
                        alert("Error parsing CSV file. Please ensure it's a valid CSV generated by this application.\n" + error.message);
                    }
                };
                reader.onerror = function() {
                    alert("Error reading file.");
                };
                reader.readAsText(file);
            }
            event.target.value = null; // Reset file input to allow loading the same file again
        });

        function parseCSV(csvText) {
            const lines = csvText.trim().split('\n');
            if (lines.length < 2) return []; // Must have headers and at least one data row

            const headers = lines[0].split(',').map(h => h.trim());
            const entries = [];

            for (let i = 1; i < lines.length; i++) {
                const values = parseCsvRow(lines[i]); // Use a robust row parser
                if (values.length === headers.length) {
                    const entry = {};
                    headers.forEach((header, index) => {
                        entry[header] = values[index];
                    });
                    entries.push(entry);
                } else {
                    console.warn(`Skipping malformed CSV line ${i+1}: Expected ${headers.length} values, got ${values.length}`);
                }
            }
            return entries;
        }

        function parseCsvRow(rowString) { // Handles simple CSV with quoted fields
            const regex = /(?:^|,)(\"(?:[^\"]+|\"\")*\"|[^,]*)/g;
            let matches;
            const values = [];
            while ((matches = regex.exec(rowString)) !== null) {
                let value = matches[1];
                if (value.startsWith('"') && value.endsWith('"')) {
                    value = value.substring(1, value.length - 1).replace(/""/g, '"');
                }
                values.push(value);
            }
            return values;
        }



        // Download CSV button handling
        document.getElementById('downloadCsvBtn').addEventListener('click', () => {
            const entries = JSON.parse(localStorage.getItem('bitEntries') || '[]');

            if (entries.length === 0) {
                alert('No entries to download.');
                return;
            }

            // Prepare CSV content from all entries in localStorage
            const headers = Object.keys(entries[0]).join(',');
            const dataRows = entries.map(entry => {
                return Object.values(entry).map(value => {
                    let val = String(value || ''); // Ensure value is a string, handle null/undefined
                    // Escape commas, double quotes, and newlines within a field
                    if (val.includes(',') || val.includes('"') || val.includes('\n')) {
                        val = `"${val.replace(/"/g, '""')}"`; // Enclose in quotes, double up existing quotes
                    }
                    return val;
                }).join(',');
            }).join('\n');

            const csvContent = headers + '\n' + dataRows;

            // Create a Blob with the CSV data
            const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });

            // Create a link element to trigger download
            const link = document.createElement("a");
            if (link.download !== undefined) { // Check if HTML5 download attribute is supported
                const url = URL.createObjectURL(blob);
                link.setAttribute("href", url);
                link.setAttribute("download", "datasheet.csv"); // Suggested filename
                link.style.visibility = 'hidden';
                document.body.appendChild(link);
                link.click();
                document.body.removeChild(link);
                URL.revokeObjectURL(url); // Clean up
                alert('All entries prepared for download as datasheet.csv!');
            } else {
                alert("Your browser does not support direct file download. Please consider using a modern browser to download data as CSV.");
            }
        });

        // Initial display of entries on page load
        displayEntries();
    </script>
</body>
</html>
