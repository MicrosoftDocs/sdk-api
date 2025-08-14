---
UID: NF:winbase.ReplaceFileW
title: ReplaceFileW function (winbase.h)
description: Replaces one file with another file, with the option of creating a backup copy of the original file. (Unicode)
helpviewer_keywords: ["REPLACEFILE_IGNORE_ACL_ERRORS", "REPLACEFILE_IGNORE_MERGE_ERRORS", "REPLACEFILE_WRITE_THROUGH", "ReplaceFile", "ReplaceFile function [Files]", "ReplaceFileW", "_win32_replacefile", "base.replacefile", "fs.replacefile", "winbase/ReplaceFile", "winbase/ReplaceFileW"]
old-location: fs\replacefile.htm
tech.root: fs
ms.assetid: 23402a71-e945-4891-9815-c75e57051501
ms.date: 12/05/2018
ms.keywords: REPLACEFILE_IGNORE_ACL_ERRORS, REPLACEFILE_IGNORE_MERGE_ERRORS, REPLACEFILE_WRITE_THROUGH, ReplaceFile, ReplaceFile function [Files], ReplaceFileA, ReplaceFileW, _win32_replacefile, base.replacefile, fs.replacefile, winbase/ReplaceFile, winbase/ReplaceFileA, winbase/ReplaceFileW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReplaceFileW (Unicode) and ReplaceFileA (ANSI)
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
 - ReplaceFileW
 - winbase/ReplaceFileW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l2-1-4.dll
 - api-ms-win-core-file-l2-1-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-Ms-Win-Core-File-Ansi-L2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - ReplaceFile
 - ReplaceFileA
 - ReplaceFileW
---

# ReplaceFileW function


## -description

Replaces one file with another file, with the option of creating a backup copy of the original 
    file. The replacement file assumes the name of the replaced file and its identity.

## -parameters

### -param lpReplacedFileName [in]

The name of the file to be replaced.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.


This file is opened with the <b>GENERIC_READ</b>, <b>DELETE</b>, and 
       <b>SYNCHRONIZE</b> access rights. The sharing mode is 
       <b>FILE_SHARE_READ</b> | <b>FILE_SHARE_WRITE</b> | 
       <b>FILE_SHARE_DELETE</b>.

The caller must have write access to the file to be replaced. For more information, see 
       <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param lpReplacementFileName [in]

The name of the file that will replace the <i>lpReplacedFileName</i> file.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.


The function attempts to open this file with the <b>SYNCHRONIZE</b>, 
       <b>GENERIC_READ</b>, <b>GENERIC_WRITE</b>, 
       <b>DELETE</b>, and <b>WRITE_DAC</b> access rights so that it can preserve 
       all attributes and ACLs. If this fails, the function attempts to open the file with the 
       <b>SYNCHRONIZE</b>, <b>GENERIC_READ</b>, 
       <b>DELETE</b>, and <b>WRITE_DAC</b> access rights. No sharing mode is 
       specified.

### -param lpBackupFileName [in, optional]

The name of the file that will serve as a backup copy of the <i>lpReplacedFileName</i> 
       file. If this parameter is <b>NULL</b>, no backup file is created. See the Remarks section for implementation details on the backup file. 

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param dwReplaceFlags [in]

The replacement options. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REPLACEFILE_WRITE_THROUGH"></a><a id="replacefile_write_through"></a><dl>
<dt><b>REPLACEFILE_WRITE_THROUGH</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="REPLACEFILE_IGNORE_MERGE_ERRORS"></a><a id="replacefile_ignore_merge_errors"></a><dl>
<dt><b>REPLACEFILE_IGNORE_MERGE_ERRORS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Ignores errors that occur while merging information (such as attributes and ACLs) from the replaced file to 
         the replacement file. Therefore, if you specify this flag and do not have <b>WRITE_DAC</b> 
         access, the function succeeds but the ACLs are not preserved.

</td>
</tr>
<tr>
<td width="40%"><a id="REPLACEFILE_IGNORE_ACL_ERRORS"></a><a id="replacefile_ignore_acl_errors"></a><dl>
<dt><b>REPLACEFILE_IGNORE_ACL_ERRORS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Ignores errors that occur while merging ACL information from the replaced file to the replacement file. 
         Therefore, if you specify this flag and do not have <b>WRITE_DAC</b> access, the function 
         succeeds but the ACLs are not preserved. To compile an application that uses this value, define the 
         <b>_WIN32_WINNT</b> macro as 0x0600 or later.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -param lpExclude

Reserved for future use.

### -param lpReserved

Reserved for future use.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following are possible error codes 
       for this function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNABLE_TO_MOVE_REPLACEMENT</b></dt>
<dt>1176 (0x498)</dt>
</dl>
</td>
<td width="60%">
The replacement file could not be renamed. If <i>lpBackupFileName</i> was specified, 
         the replaced and replacement files retain their original file names. Otherwise, the replaced file no longer 
         exists and the replacement file exists under its original name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNABLE_TO_MOVE_REPLACEMENT_2</b></dt>
<dt>1177 (0x499)</dt>
</dl>
</td>
<td width="60%">
The replacement file could not be moved.  The replacement file still exists under its original name; 
         however, it has inherited the file streams and attributes from the file it is replacing. The file to be 
         replaced still exists with a different name. If <i>lpBackupFileName</i> is specified, it 
         will be the name of the replaced file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNABLE_TO_REMOVE_REPLACED</b></dt>
<dt>1175 (0x497)</dt>
</dl>
</td>
<td width="60%">
The replaced file could not be deleted. The replaced and replacement files retain their original file 
         names.

</td>
</tr>
</table>
 

If any other error is returned, such as <b>ERROR_INVALID_PARAMETER</b>, the replaced and 
       replacement files will retain their original file names. In this scenario, a backup file 
       does not exist and it is not guaranteed that the 
       replacement file will have inherited all of the attributes and streams of the replaced file.

## -remarks

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>ReplaceFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation. See the "Maximum Path Length Limitation" section of <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>
The <b>ReplaceFile</b> function combines several steps within a 
     single function. An application can call <b>ReplaceFile</b> instead 
     of calling separate functions to save the data to a new file, rename the original file using a temporary name, 
     rename the new file to have the same name as the original file, and delete the original file. Another advantage is 
     that <b>ReplaceFile</b> not only copies the new file data, but also 
     preserves the following attributes of the original file:

<ul>
<li>Creation time</li>
<li>Short file name</li>
<li>Object identifier</li>
<li>DACLs</li>
<li>Security resource attributes</li>
<li>Encryption</li>
<li>Compression</li>
<li>Named streams not already in the replacement file</li>
</ul>
For example, if the replacement file is encrypted, but the replaced file is not encrypted, the resulting file 
     is not encrypted.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Security resource attributes (<b>ATTRIBUTE_SECURITY_INFORMATION</b>) for the original 
      file are not preserved until Windows 8 and Windows Server 2012.

<div class="alert"><b>Note</b>  <p class="note">If the replacement file is protected using <a href="/previous-versions/windows/dn440592(v=win.10)">Selective Wipe</a>, then the replaced file will be protected by the enterprise id of the replacement file.

</div>
<div> </div>
The resulting file has the same file ID as the replacement file.

The backup file, replaced file, and replacement file must all reside on the same volume.

To delete or rename a file, you must have either delete permission on the file or delete child permission in 
     the parent directory. If you set up a directory with all access except delete and delete child and the DACLs of 
     new files are inherited, then you should be able to create a file without being able to delete it. However, you 
     can then create a file, and you will get all the access you request on the handle returned to you at the time you 
     create the file. If you requested delete permission at the time you created the file, you could delete or rename 
     the file with that handle but not with any other.





> [!NOTE]
> The winbase.h header defines ReplaceFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-copyfile">CopyFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-copyfileexa">CopyFileEx</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefile">MoveFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefileexa">MoveFileEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefilewithprogressa">MoveFileWithProgress</a>
