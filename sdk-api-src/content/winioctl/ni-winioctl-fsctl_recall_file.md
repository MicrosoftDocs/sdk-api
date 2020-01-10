---
UID: NI:winioctl.FSCTL_RECALL_FILE
title: FSCTL_RECALL_FILE
description: Recalls a file from storage media that Remote Storage manages, which is the hierarchical storage management software.
old-location: fs\fsctl_recall_file.htm
tech.root: FileIO
ms.assetid: f131203b-6d8e-4445-9b4f-a24e1ca62645
ms.date: 12/05/2018
ms.keywords: FSCTL_RECALL_FILE, FSCTL_RECALL_FILE control, FSCTL_RECALL_FILE control code [Files], _win32_fsctl_recall_file, base.fsctl_recall_file, fs.fsctl_recall_file, winioctl/FSCTL_RECALL_FILE
f1_keywords:
- winioctl/FSCTL_RECALL_FILE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- FSCTL_RECALL_FILE
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_RECALL_FILE IOCTL


## -description


Recalls a file from storage media that Remote Storage manages, which is the hierarchical storage management software.

To recall a file, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to file or directory
  FSCTL_RECALL_FILE,           // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSizeNULL,                        // lpOutBuffer0,                           // nOutBufferSize(LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);</pre>
</td>
</tr>
</table></span></div>

## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



<b>FSCTL_RECALL_FILE</b> recovers a file from storage, for example,  a tape that is managed by Remote Storage. If the file is already cached locally, this operation does nothing. Similarly, if the file has not been moved to remote storage, this operation does nothing.

<b>FSCTL_RECALL_FILE</b> operates only on systems where Remote Storage is installed. If Remote Storage is not installed, the operation fails and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the error code <b>ERROR_INVALID_FUNCTION</b>.

Directories cannot be moved to remote storage. Calling 
<b>FSCTL_RECALL_FILE</b> for a directory fails, and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the error code <b>ERROR_INVALID_HANDLE</b>.

Typically, files that are stored on media that is managed by Remote Storage are recalled when an application attempts to make the first access to data. An application that opens a file without immediately accessing the data can speed up the first access by using 
<b>FSCTL_RECALL_FILE</b> immediately after opening the file. However, avoid indiscriminate recall of files that an application does not touch.

Before you call 
<b>FSCTL_RECALL_FILE</b> you do not need to test a file's attributes for the flag <b>FILE_ATTRIBUTE_OFFLINE</b> with the function 
<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>. The test is unnecessary because an online file is not affected by this operation. However, any operating system call takes processor time. To conserve processor time, call 
<b>GetFileAttributes</b> to check file attributes to determine if 
<b>FSCTL_RECALL_FILE</b> is necessary.

For the implications of overlapped I/O on this operation, see the Remarks section of the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 


#### Examples

The following code example is a command-line utility that recalls one or more files indicated on the command line from remote storage.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;Windows.h&gt;
#include &lt;malloc.h&gt;
#include &lt;stdio.h&gt;
#include &lt;WinIoCtl.h&gt;

DWORD RecallFile(PTCHAR FileName);

int _cdecl _tmain(int argc, TCHAR *argv[])
{
  LONG i;

  if (argc &lt; 2) {
    printf("Usage: recall &lt;file-name1&gt; &lt;file-name2&gt; ...\n");
    return 1;
  }

  for (i = 1; i &lt; argc; i++) {
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
                       &amp;nbytes,
                       NULL)) 
  {
    errorCode = GetLastError();
    printf("Couldn't recall file %s: error %x\n", 
           FileName, errorCode);
  }
  CloseHandle(fileHandle);
  return errorCode;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>
 

 

