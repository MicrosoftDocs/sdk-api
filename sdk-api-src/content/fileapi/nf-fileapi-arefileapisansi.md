---
UID: NF:fileapi.AreFileApisANSI
title: AreFileApisANSI function (fileapi.h)
description: Determines whether the file I/O functions are using the ANSI or OEM character set code page.
helpviewer_keywords: ["AreFileApisANSI","AreFileApisANSI function [Files]","_win32_arefileapisansi","base.arefileapisansi","fileapi/AreFileApisANSI","fs.arefileapisansi"]
old-location: fs\arefileapisansi.htm
tech.root: fs
ms.assetid: 6bebe896-86d1-40b8-ab7f-0305ada71fdf
ms.date: 12/05/2018
ms.keywords: AreFileApisANSI, AreFileApisANSI function [Files], _win32_arefileapisansi, base.arefileapisansi, fileapi/AreFileApisANSI, fs.arefileapisansi
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AreFileApisANSI
 - fileapi/AreFileApisANSI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-file-l1-2-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - AreFileApisANSI
---

# AreFileApisANSI function


## -description

Determines whether the file I/O functions are using the ANSI or OEM character set code 
    page. This function is useful for 8-bit console input and output operations.



## -returns

If the set of file I/O functions is using the ANSI code page, the return value is nonzero.

If the set of file I/O functions is using the OEM code page, the return value is zero.

## -remarks

The <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem">SetFileApisToOEM</a> function causes a set of file 
    I/O functions to use the OEM code page. The 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi">SetFileApisToANSI</a> function causes the same set of file 
    I/O functions to use the ANSI code page. Use the <b>AreFileApisANSI</b> function to 
    determine which code page the set of file I/O functions is currently using. For a discussion of these functions' 
    usage, please see the Remarks sections of 
    <b>SetFileApisToOEM</b> and 
    <b>SetFileApisToANSI</b>.

The file I/O functions whose code page is ascertained by <b>AreFileApisANSI</b> are 
    those functions exported by KERNEL32.DLL that accept or return a file name.

The functions <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem">SetFileApisToOEM</a> and 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi">SetFileApisToANSI</a> set the code page for a process, so 
    <b>AreFileApisANSI</b> returns a value indicating the code page of an entire 
    process.

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

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi">SetFileApisToANSI</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem">SetFileApisToOEM</a>
