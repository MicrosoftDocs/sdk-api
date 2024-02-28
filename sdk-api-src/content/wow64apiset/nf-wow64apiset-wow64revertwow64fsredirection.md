---
UID: NF:wow64apiset.Wow64RevertWow64FsRedirection
title: Wow64RevertWow64FsRedirection function (wow64apiset.h)
description: Restores file system redirection for the calling thread.
helpviewer_keywords: ["Wow64RevertWow64FsRedirection","Wow64RevertWow64FsRedirection function [Files]","base.wow64revertwow64fsredirection","fs.wow64revertwow64fsredirection","wow64apiset/Wow64RevertWow64FsRedirection"]
old-location: fs\wow64revertwow64fsredirection.htm
tech.root: fs
ms.assetid: 8a09bdeb-b969-48b2-a432-c78dd4177000
ms.date: 04/14/2022
ms.keywords: Wow64RevertWow64FsRedirection, Wow64RevertWow64FsRedirection function [Files], base.wow64revertwow64fsredirection, fs.wow64revertwow64fsredirection, wow64apiset/Wow64RevertWow64FsRedirection
req.header: wow64apiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Wow64RevertWow64FsRedirection
 - wow64apiset/Wow64RevertWow64FsRedirection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Wow64-l1-1-0.dll
 - API-MS-Win-Core-Wow64-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - Wow64RevertWow64FsRedirection
---

# Wow64RevertWow64FsRedirection function

## -description

Restores file system redirection for the calling thread.

This function should not be called without a previous call to the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> function.

Any data allocation on behalf of the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> function is cleaned up by this function.

## -parameters

### -param OlValue [in]

The WOW64 file system redirection value. This value is obtained from the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> function.

This value is defined in `wow64apiset.h`.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is <b>FALSE</b> (zero). To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a>/<b>Wow64RevertWow64FsRedirection</b> function pair is a replacement for the functionality of the <a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64enablewow64fsredirection">Wow64EnableWow64FsRedirection</a> function.

To disable file system redirection, call the [Wow64DisableWow64FsRedirection](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection) function. Every call to the **Wow64DisableWow64FsRedirection** function must have a matching call to the  **Wow64RevertWow64FsRedirection** function. This will ensure redirection is re-enabled and frees associated system resources.

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
Yes

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

### Examples

For an example, see the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> function.

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>

<a href="/windows/desktop/WinProg64/file-system-redirector">File System Redirector</a>

<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a>

<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64enablewow64fsredirection">Wow64EnableWow64FsRedirection</a>
