# NodeJs File System API Documentation
 
This API allows you to create and read text files in a specific directory.

### Base URL

http://localhost:3000

# Create File Endpoint

**GET /createfile**

#### Description:

This endpoint creates a text file in the "files" directory with the current timestamp as the file name and content.

#### Request Parameters:

None

#### Response:

- **200 OK**: File created successfully.
- **404 Not Found**: Error occurred while creating the file.

#### Example:
-------------

**Request:**

**GET /createfile:**


**Response (Success):**

```json
{
    "message": "File Created Successfully",
    "fileName": "19-3-2024_0-16-14PM.txt"
}
```

**Response (Error):**
```json
{
  "message": "Error Occurred"
}
```
--------------------------

# Read File Endpoint
**GET /readfile**

#### Description:
This endpoint retrieves all text files in the "files" directory.

#### Request Parameters:
None

#### Response:
- **200 OK**: List of text files found in the directory.
- **404 Not Found**: Error occurred while reading the files or no files found.

#### Example
------------
**Request:**
**GET /readfile**

**Response (Success):**
```json
{
    "files": [
        "19-3-2024_4-47-42PM.txt",
        "19-3-2024_4-55-14PM.txt",
        "19-3-2024_4-57-35PM.txt"
    ]
}
```

**Response (No Files Found):**
```json
{
  "message": "No Files Found"
}
```
**Response (Error):**
```json
{
  "message": "Error Occurred"
}
```
