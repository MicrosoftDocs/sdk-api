---
UID: NF:winbase.CopyFile2
title: CopyFile2 function (winbase.h)
description: Copies an existing file to a new file, notifying the application of its progress through a callback function.
old-location: fs\copyfile2.htm
tech.root: FileIO
ms.assetid: aa2df686-4b61-4d90-ba0b-c78c5a0d2d59
ms.date: 12/05/2018
ms.keywords: CopyFile2, CopyFile2 function [Files], fs.copyfile2, winbase/CopyFile2
f1_keywords:
- winbase/CopyFile2
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-File-l2-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-File-l2-1-1.dll
- API-MS-Win-Core-File-l2-1-2.dll
api_name:
- CopyFile2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CopyFile2 function


## -description


Copies an existing file to a new file, notifying the application of its progress through a callback 
    function.


## -parameters




### -param pwszExistingFileName [in]

The name of an existing file.

To extend this limit to 32,767 wide characters, prepend "\\?\" to the path. For more 
       information, see <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\".  See the "Maximum Path Limitation" section of  <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>
If <i>lpExistingFileName</i> does not exist, the 
       <b>CopyFile2</b> function fails returns 
       <code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code>.


### -param pwszNewFileName [in]

The name of the new file.

To extend this limit to 32,767 wide characters, prepend "\\?\" to the path. For more 
       information, see <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

### -param pExtendedParameters [in, optional]

Optional address of a 
      <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a> 
      structure.


## -returns



If the function succeeds, the return value will return <b>TRUE</b> when passed to the 
      <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> macro.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The copy operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_REQUEST_PAUSED)</b></dt>
</dl>
</td>
<td width="60%">
The copy operation was paused by a <b>COPYFILE2_PROGRESS_PAUSE</b> return from the 
        <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback 
        function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_REQUEST_ABORTED)</b></dt>
</dl>
</td>
<td width="60%">
The copy operation was paused by a <b>COPYFILE2_PROGRESS_CANCEL</b> or 
        <b>COPYFILE2_PROGRESS_STOP</b> return from the 
        <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback 
        function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwCopyFlags</b> member of the 
        <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a> structure 
        passed through the <i>pExtendedParameters</i> parameter contains the 
        <b>COPY_FILE_FAIL_IF_EXISTS</b> flag and a conflicting name existed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwCopyFlags</b> member of the 
        <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a> structure 
        passed through the <i>pExtendedParameters</i> parameter contains the 
        <b>COPY_FILE_FAIL_IF_EXISTS</b> flag and a conflicting name existed.

</td>
</tr>
</table>
 




## -remarks



This function preserves extended attributes, OLE structured storage, NTFS file system alternate data streams, 
    and file attributes. Security attributes for the existing file are not copied to the new file. To copy security 
    attributes, use the <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.

This function fails with 
    <code>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</code> if the destination 
    file already exists and has the <b>FILE_ATTRIBUTE_HIDDEN</b> or 
    <b>FILE_ATTRIBUTE_READONLY</b> attribute set.

To compile an application that uses this function, define the <b>_WIN32_WINNT</b> macro 
    as <b>_WIN32_WINNT_WIN8</b> or later. For more information, see 
    <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-functions">File Management Functions</a>
 

 

