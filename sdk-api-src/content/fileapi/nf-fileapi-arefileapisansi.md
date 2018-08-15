---
UID: NF:fileapi.AreFileApisANSI
title: AreFileApisANSI function
author: windows-sdk-content
description: Determines whether the file I/O functions are using the ANSI or OEM character set code page.
old-location: fs\arefileapisansi.htm
old-project: fileio
ms.assetid: 6bebe896-86d1-40b8-ab7f-0305ada71fdf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AreFileApisANSI, AreFileApisANSI function [Files], _win32_arefileapisansi, base.arefileapisansi, fileapi/AreFileApisANSI, fs.arefileapisansi
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.redist: 
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
tech.root: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-file-l1-2-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - AreFileApisANSI
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# AreFileApisANSI function


## -description


Determines whether the file I/O functions are using the ANSI or OEM character set code 
    page. This function is useful for 8-bit console input and output operations.


## -parameters






## -returns



If the set of file I/O functions is using the ANSI code page, the return value is nonzero.

If the set of file I/O functions is using the OEM code page, the return value is zero.




## -remarks



The <a href="https://msdn.microsoft.com/15f657d8-075a-4f0c-a653-73273ea62f5f">SetFileApisToOEM</a> function causes a set of file 
    I/O functions to use the OEM code page. The 
    <a href="https://msdn.microsoft.com/72b19773-9663-4cf8-90d3-656ee2785601">SetFileApisToANSI</a> function causes the same set of file 
    I/O functions to use the ANSI code page. Use the <b>AreFileApisANSI</b> function to 
    determine which code page the set of file I/O functions is currently using. For a discussion of these functions' 
    usage, please see the Remarks sections of 
    <b>SetFileApisToOEM</b> and 
    <b>SetFileApisToANSI</b>.

The file I/O functions whose code page is ascertained by <b>AreFileApisANSI</b> are 
    those functions exported by KERNEL32.DLL that accept or return a file name.

The functions <a href="https://msdn.microsoft.com/15f657d8-075a-4f0c-a653-73273ea62f5f">SetFileApisToOEM</a> and 
    <a href="https://msdn.microsoft.com/72b19773-9663-4cf8-90d3-656ee2785601">SetFileApisToANSI</a> set the code page for a process, so 
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




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/72b19773-9663-4cf8-90d3-656ee2785601">SetFileApisToANSI</a>



<a href="https://msdn.microsoft.com/15f657d8-075a-4f0c-a653-73273ea62f5f">SetFileApisToOEM</a>
 

 

