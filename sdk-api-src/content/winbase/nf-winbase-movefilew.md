---
UID: NF:winbase.MoveFileW
title: MoveFileW function
author: windows-sdk-content
description: Moves an existing file or a directory, including its children.
old-location: fs\movefile.htm
old-project: FileIO
ms.assetid: baa3cc02-0a61-4463-b2f1-0d7aaefa126b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: MoveFile, MoveFile function [Files], MoveFileA, MoveFileW, _win32_movefile, base.movefile, fs.movefile, rename file [Files], winbase/MoveFile, winbase/MoveFileA, winbase/MoveFileW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MoveFileW (Unicode) and MoveFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	MoveFile
-	MoveFileA
-	MoveFileW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# MoveFileW function


## -description


Moves an existing file or a directory, including its children.

To specify how to move the file, use the 
    <a href="https://msdn.microsoft.com/5fb4f897-66ed-49d7-913a-fb6e7cecdfa3">MoveFileEx</a> or 
    <a href="https://msdn.microsoft.com/f490aadc-7934-498a-8131-5c1be9e6f1aa">MoveFileWithProgress</a> function.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/466d733b-30d2-4297-a0e6-77038f1a21d5">MoveFileTransacted</a> function.


## -parameters




### -param lpExistingFileName [in]

The current name of the file or directory on the local computer.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>MoveFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpNewFileName [in]

The new name for the file or directory. The new name must not already exist. A new file may be on a 
       different file system or drive. A new directory must be on the same drive.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>MoveFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>MoveFile</b> function will move (rename) either a file or a 
    directory (including its children) either in the same directory or across directories. The one caveat is that the 
    <b>MoveFile</b> function will fail on directory moves when the 
    destination is on a different volume.

 If a file is moved across volumes, <b>MoveFile</b> does not move 
    the security descriptor with the file. The file will be assigned the default security descriptor in the 
    destination directory.

The <b>MoveFile</b> function coordinates its operation with the 
    link tracking service, so link sources can be tracked as they are moved.

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
See comment

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
See comment

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
 

SMB 3.0 does not support rename of alternate data streams on file shares with continuous availability capability.




## -see-also




<a href="https://msdn.microsoft.com/2c8ad002-cef4-499c-acda-c162205f6a8d">CopyFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/5fb4f897-66ed-49d7-913a-fb6e7cecdfa3">MoveFileEx</a>



<a href="https://msdn.microsoft.com/466d733b-30d2-4297-a0e6-77038f1a21d5">MoveFileTransacted</a>



<a href="https://msdn.microsoft.com/f490aadc-7934-498a-8131-5c1be9e6f1aa">MoveFileWithProgress</a>
 

 

