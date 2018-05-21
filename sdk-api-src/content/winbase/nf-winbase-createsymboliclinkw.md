---
UID: NF:winbase.CreateSymbolicLinkW
title: CreateSymbolicLinkW function
author: windows-driver-content
description: Creates a symbolic link.
old-location: fs\createsymboliclink.htm
old-project: FileIO
ms.assetid: 9e7c70b5-ced1-4cd4-b8b9-0ad3385e5437
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CreateSymbolicLink, CreateSymbolicLink function [Files], CreateSymbolicLinkA, CreateSymbolicLinkW, SYMBOLIC_LINK_FLAG_ALLOW_UNPRIVILEGED_CREATE, SYMBOLIC_LINK_FLAG_DIRECTORY, fs.createsymboliclink, winbase/CreateSymbolicLink, winbase/CreateSymbolicLinkA, winbase/CreateSymbolicLinkW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateSymbolicLinkW (Unicode) and CreateSymbolicLinkA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l2-1-1.dll
-	API-MS-Win-Core-File-l2-1-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	API-Ms-Win-Core-File-Ansi-L2-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	CreateSymbolicLink
-	CreateSymbolicLinkA
-	CreateSymbolicLinkW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateSymbolicLinkW function


## -description


Creates a symbolic link.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/e440b940-129b-4638-a0b5-8f516687c74e">CreateSymbolicLinkTransacted</a> function.


## -parameters




### -param lpSymlinkFileName [in]

The symbolic link to be created.

This parameter may include the path. In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CreateSymbolicLinkW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpTargetFileName [in]

The name of the target for the symbolic link to be created.

 If <i>lpTargetFileName</i> has a device name associated with it, the link is treated as 
      an absolute link; otherwise, the link is treated as a relative link.

This parameter may include the path. In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CreateSymbolicLinkW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param dwFlags [in]

Indicates whether the link target, <i>lpTargetFileName</i>, is a directory.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The link target is a file.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMBOLIC_LINK_FLAG_DIRECTORY"></a><a id="symbolic_link_flag_directory"></a><dl>
<dt><b>SYMBOLIC_LINK_FLAG_DIRECTORY</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The link target is a directory.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMBOLIC_LINK_FLAG_ALLOW_UNPRIVILEGED_CREATE"></a><a id="symbolic_link_flag_allow_unprivileged_create"></a><dl>
<dt><b>SYMBOLIC_LINK_FLAG_ALLOW_UNPRIVILEGED_CREATE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Specify this flag to allow creation of symbolic links when the process is not elevated.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Symbolic links can either be absolute or relative links. Absolute links are links that specify each portion of 
    the path name; relative links are determined relative to where relative–link specifiers are 
    in a specified path. Relative links are specified using the following conventions:

<ul>
<li>Dot (. and ..) conventions—for example, 
      "..\" resolves the path relative to the parent directory.</li>
<li>Names with no slashes (\)—for example, "tmp" resolves 
      the path relative to the current directory.</li>
<li>Root relative—for example, "\Windows\System32" resolves 
      to "<i>current drive</i>:\Windows\System32".</li>
<li>Current working directory–relative—for example, if the current 
      working directory is C:\Windows\System32, "C:File.txt" resolves to 
      "C:\Windows\System32\File.txt".
      <div class="alert"><b>Note</b>  If you specify a current working directory–relative link, it is created as an 
       absolute link, due to the way the current working directory is processed based on the user and the 
       thread.</div>
<div> </div>
</li>
</ul>
To remove a symbolic link, delete the file (using 
    <a href="https://msdn.microsoft.com/0b947a85-816b-4374-a8f8-c369e366a17d">DeleteFile</a> or similar APIs) or remove the directory (using 
    <a href="https://msdn.microsoft.com/d699cdd2-e270-4f17-bdec-6eea25b01578">RemoveDirectory</a> or similar APIs) depending on what type 
    of symbolic link is used.

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
 

CsvFs does not support soft link or any other reparse points.





## -see-also




<a href="https://msdn.microsoft.com/e440b940-129b-4638-a0b5-8f516687c74e">CreateSymbolicLinkTransacted</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

