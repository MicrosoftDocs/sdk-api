---
UID: NF:winbase.CreateSymbolicLinkA
title: CreateSymbolicLinkA function (winbase.h)
description: Creates a symbolic link. (ANSI)
helpviewer_keywords: ["CreateSymbolicLinkA", "SYMBOLIC_LINK_FLAG_ALLOW_UNPRIVILEGED_CREATE", "SYMBOLIC_LINK_FLAG_DIRECTORY", "winbase/CreateSymbolicLinkA"]
old-location: fs\createsymboliclink.htm
tech.root: fs
ms.assetid: 9e7c70b5-ced1-4cd4-b8b9-0ad3385e5437
ms.date: 12/05/2018
ms.keywords: CreateSymbolicLink, CreateSymbolicLink function [Files], CreateSymbolicLinkA, CreateSymbolicLinkW, SYMBOLIC_LINK_FLAG_ALLOW_UNPRIVILEGED_CREATE, SYMBOLIC_LINK_FLAG_DIRECTORY, fs.createsymboliclink, winbase/CreateSymbolicLink, winbase/CreateSymbolicLinkA, winbase/CreateSymbolicLinkW
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateSymbolicLinkA
 - winbase/CreateSymbolicLinkA
dev_langs:
 - c++
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
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-Ms-Win-Core-File-Ansi-L2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - CreateSymbolicLink
 - CreateSymbolicLinkA
 - CreateSymbolicLinkW
---

# CreateSymbolicLinkA function


## -description

Creates a symbolic link.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-createsymboliclinktransacteda">CreateSymbolicLinkTransacted</a> function.

## -parameters

### -param lpSymlinkFileName [in]

The symbolic link to be created.

This parameter may include the path. 

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpTargetFileName [in]

The name of the target for the symbolic link to be created.

 If <i>lpTargetFileName</i> has a device name associated with it, the link is treated as 
      an absolute link; otherwise, the link is treated as a relative link.

This parameter may include the path. 

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

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
Specify this flag to allow creation of symbolic links when the process is not elevated. In UWP, <a href="/windows/uwp/get-started/enable-your-device-for-development">Developer Mode</a> must first be enabled on the machine before  this option will function.  Under MSIX, developer mode is not required to be enabled for this flag.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Symbolic links can either be absolute or relative links. Absolute links are links that specify each portion of 
    the path name; relative links are determined relative to where relative–link specifiers are 
    in a specified path. Relative links are specified using the following conventions:

<ul>
<li>Dot (. and ..) conventions—for example, 
      "..\" resolves the path relative to the parent directory.</li>
<li>Names with no slashes (\\)—for example, "tmp" resolves 
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
    <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a> or similar APIs) or remove the directory (using 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-removedirectorya">RemoveDirectory</a> or similar APIs) depending on what type 
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






> [!NOTE]
> The winbase.h header defines CreateSymbolicLink as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createsymboliclinktransacteda">CreateSymbolicLinkTransacted</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
