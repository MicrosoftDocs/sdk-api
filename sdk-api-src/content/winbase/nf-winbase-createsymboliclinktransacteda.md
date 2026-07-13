---
UID: NF:winbase.CreateSymbolicLinkTransactedA
title: CreateSymbolicLinkTransactedA function (winbase.h)
description: Creates a symbolic link as a transacted operation. (ANSI)
helpviewer_keywords: ["CreateSymbolicLinkTransactedA", "SYMBOLIC_LINK_FLAG_DIRECTORY", "winbase/CreateSymbolicLinkTransactedA"]
old-location: fs\createsymboliclinktransacted.htm
tech.root: fs
ms.assetid: e440b940-129b-4638-a0b5-8f516687c74e
ms.date: 12/05/2018
ms.keywords: CreateSymbolicLinkTransacted, CreateSymbolicLinkTransacted function [Files], CreateSymbolicLinkTransactedA, CreateSymbolicLinkTransactedW, SYMBOLIC_LINK_FLAG_DIRECTORY, fs.createsymboliclinktransacted, winbase/CreateSymbolicLinkTransacted, winbase/CreateSymbolicLinkTransactedA, winbase/CreateSymbolicLinkTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateSymbolicLinkTransactedW (Unicode) and CreateSymbolicLinkTransactedA (ANSI)
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
 - CreateSymbolicLinkTransactedA
 - winbase/CreateSymbolicLinkTransactedA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - CreateSymbolicLinkTransacted
 - CreateSymbolicLinkTransactedA
 - CreateSymbolicLinkTransactedW
---

# CreateSymbolicLinkTransactedA function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Creates a symbolic link as a transacted operation.

## -parameters

### -param lpSymlinkFileName [in]

The symbolic link to be created.

### -param lpTargetFileName [in]

The name of the target for the symbolic link to be created.

If <i>lpTargetFileName</i> has a device name associated with it, the link is treated as an 
       absolute link; otherwise, the link is treated as a relative link.

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
</table>

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

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
No

</td>
</tr>
</table>
 

SMB 3.0 does not support TxF.





> [!NOTE]
> The winbase.h header defines CreateSymbolicLinkTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
