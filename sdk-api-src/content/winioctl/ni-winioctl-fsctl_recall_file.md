---
UID: NI:winioctl.FSCTL_RECALL_FILE
title: FSCTL_RECALL_FILE
description: Recalls a file from storage media that Remote Storage manages, which is the hierarchical storage management software.
helpviewer_keywords: ["FSCTL_RECALL_FILE","FSCTL_RECALL_FILE control","FSCTL_RECALL_FILE control code [Files]","_win32_fsctl_recall_file","base.fsctl_recall_file","fs.fsctl_recall_file","winioctl/FSCTL_RECALL_FILE"]
old-location: fs\fsctl_recall_file.htm
tech.root: fs
ms.assetid: f131203b-6d8e-4445-9b4f-a24e1ca62645
ms.date: 12/05/2018
ms.keywords: FSCTL_RECALL_FILE, FSCTL_RECALL_FILE control, FSCTL_RECALL_FILE control code [Files], _win32_fsctl_recall_file, base.fsctl_recall_file, fs.fsctl_recall_file, winioctl/FSCTL_RECALL_FILE
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - FSCTL_RECALL_FILE
 - winioctl/FSCTL_RECALL_FILE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_RECALL_FILE
---

# FSCTL_RECALL_FILE IOCTL


## -description

Recalls a file from storage media that Remote Storage manages, which is the hierarchical storage management software.

To recall a file, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file or directory
  FSCTL_RECALL_FILE,                // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  NULL,                             // lpOutBuffer
  0,                                // nOutBufferSize
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

**FSCTL_RECALL_FILE** recovers a file from storage, for example,  a tape that is managed by Remote Storage. If the file is already cached locally, this operation does nothing. Similarly, if the file has not been moved to remote storage, this operation does nothing.

**FSCTL_RECALL_FILE** operates only on systems where Remote Storage is installed. If Remote Storage is not installed, the operation fails and [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns the error code **ERROR_INVALID_FUNCTION**.

Directories cannot be moved to remote storage. Calling **FSCTL_RECALL_FILE** for a directory fails, and [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns the error code **ERROR_INVALID_HANDLE**.

Typically, files that are stored on media that is managed by Remote Storage are recalled when an application attempts to make the first access to data. An application that opens a file without immediately accessing the data can speed up the first access by using **FSCTL_RECALL_FILE** immediately after opening the file. However, avoid indiscriminate recall of files that an application does not touch.

Before you call **FSCTL_RECALL_FILE** you do not need to test a file's attributes for the flag **FILE_ATTRIBUTE_OFFLINE** with the function [GetFileAttributes](../fileapi/nf-fileapi-getfileattributesa.md). The test is unnecessary because an online file is not affected by this operation. However, any operating system call takes processor time. To conserve processor time, call **GetFileAttributes** to check file attributes to determine if **FSCTL_RECALL_FILE** is necessary.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | No
Resilient File System (ReFS) | Yes


#### Examples

The following code example is a command-line utility that recalls one or more files indicated on the command line from remote storage.

```cpp
#include <Windows.h>
#include <malloc.h>
#include <stdio.h>
#include <WinIoCtl.h>

DWORD RecallFile(PTCHAR FileName);

int _cdecl _tmain(int argc, TCHAR *argv[])
{
  LONG i;

  if (argc < 2) {
    printf("Usage: recall <file-name1> <file-name2> ...\n");
    return 1;
  }

  for (i = 1; i < argc; i++) {
    (void) RecallFile((PTCHAR) argv[i]);
  }
  return 0;
}

DWORD RecallFile(IN PTCHAR FileName)
  /*++
Routine Description
    Recalls the file with the supplied path.
Arguments
    FileName - Path of the file to be recalled
Return Value
    0                   - Recall is successful.
    Any other value     - Error code for the operation.

--*/

{
  HANDLE fileHandle;
  DWORD  nbytes;
  DWORD  errorCode = 0;

  fileHandle = CreateFile((LPCTSTR) FileName,
                          GENERIC_READ,
                          FILE_SHARE_READ,
                          NULL,
                          OPEN_EXISTING,
                          FILE_ATTRIBUTE_NORMAL,
                          NULL);

  if (fileHandle == INVALID_HANDLE_VALUE) 
  {
    errorCode = GetLastError();
    printf("Couldn't open file %s: error %x\n", FileName, 
           errorCode);
    return errorCode;
  }

  if (!DeviceIoControl(fileHandle,
                       FSCTL_RECALL_FILE,
                       NULL,
                       0,
                       NULL,
                       0,
                       &nbytes,
                       NULL)) 
  {
    errorCode = GetLastError();
    printf("Couldn't recall file %s: error %x\n", 
           FileName, errorCode);
  }
  CloseHandle(fileHandle);
  return errorCode;
}
```

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)
* [GetFileAttributes](../fileapi/nf-fileapi-getfileattributesa.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)