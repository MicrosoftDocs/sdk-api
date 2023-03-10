---
UID: NF:winbase.CopyFile
title: CopyFile function (winbase.h)
description: The CopyFile function (winbase.h) copies an existing file to a new file.
helpviewer_keywords: ["CopyFile","CopyFile function [Files]","CopyFileA","CopyFileW","_win32_copyfile","base.copyfile","fs.copyfile","winbase/CopyFile","winbase/CopyFileA","winbase/CopyFileW"]
old-location: fs\copyfile.htm
tech.root: fs
ms.assetid: 2c8ad002-cef4-499c-acda-c162205f6a8d
ms.date: 08/03/2022
ms.keywords: CopyFile, CopyFile function [Files], CopyFileA, CopyFileW, _win32_copyfile, base.copyfile, fs.copyfile, winbase/CopyFile, winbase/CopyFileA, winbase/CopyFileW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CopyFileW (Unicode) and CopyFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CopyFile
 - winbase/CopyFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - CopyFile
 - CopyFileA
 - CopyFileW
---

# CopyFile function


## -description

Copies an existing file to a new file.

The <a href="/windows/desktop/api/winbase/nf-winbase-copyfileexa">CopyFileEx</a> function provides two additional 
    capabilities. <b>CopyFileEx</b> can call a specified callback 
    function each time a portion of the copy operation is completed, and 
    <b>CopyFileEx</b> can be canceled during the copy operation.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-copyfiletransacteda">CopyFileTransacted</a> function.

## -parameters

### -param lpExistingFileName [in]

The name of an existing file.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CopyFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>
If <i>lpExistingFileName</i> does not exist, 
      <b>CopyFile</b> fails, and 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
      <b>ERROR_FILE_NOT_FOUND</b>.

### -param lpNewFileName [in]

The name of the new file.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CopyFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param bFailIfExists [in]

If this parameter is <b>TRUE</b> and the new file specified by 
      <i>lpNewFileName</i> already exists, the function fails. If this parameter is 
      <b>FALSE</b> and the new file already exists, the function overwrites the existing file and 
      succeeds.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The security resource properties (<b>ATTRIBUTE_SECURITY_INFORMATION</b>) for the existing file are 
     copied to the new file.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Security resource properties for the existing file are not copied to the new file until 
      Windows 8 and Windows Server 2012.

File attributes for the existing file are copied to the new file. For example, if an existing file has the 
    <b>FILE_ATTRIBUTE_READONLY</b> file attribute, a copy created through a call to 
    <b>CopyFile</b> will also have the 
    <b>FILE_ATTRIBUTE_READONLY</b> file attribute. For more information, see 
    <a href="/windows/desktop/FileIO/retrieving-and-changing-file-attributes">Retrieving and Changing File Attributes</a>.

This function fails with <b>ERROR_ACCESS_DENIED</b> if the destination file already exists 
    and has the <b>FILE_ATTRIBUTE_HIDDEN</b> or <b>FILE_ATTRIBUTE_READONLY</b> 
    attribute set.

When <b>CopyFile</b> is used to copy an encrypted file, it attempts 
     to encrypt the destination file with the keys used in the encryption of the source file. If this cannot be done, 
     this function attempts to encrypt the destination file with default keys. If 
     neither of these methods can be done, <b>CopyFile</b> fails with an 
     <b>ERROR_ENCRYPTION_FAILED</b> error code.

Symbolic link behavior—If the source file is a symbolic link, the actual file copied is 
     the target of the symbolic link.

If the destination file already exists and is a symbolic link, the target of the symbolic link is overwritten 
     by the source file.

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
 


#### Examples

For an example, see 
     <a href="/windows/desktop/FileIO/retrieving-and-changing-file-attributes">Retrieving and Changing File Attributes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-copyfileexa">CopyFileEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-copyfiletransacteda">CopyFileTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefile">MoveFile</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
