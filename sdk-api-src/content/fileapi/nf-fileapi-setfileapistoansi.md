---
UID: NF:fileapi.SetFileApisToANSI
title: SetFileApisToANSI function
author: windows-sdk-content
description: Causes the file I/O functions to use the ANSI character set code page for the current process.
old-location: fs\setfileapistoansi.htm
old-project: fileio
ms.assetid: 72b19773-9663-4cf8-90d3-656ee2785601
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: SetFileApisToANSI, SetFileApisToANSI function [Files], _win32_setfileapistoansi, base.setfileapistoansi, fileapi/SetFileApisToANSI, fs.setfileapistoansi
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-Ms-Win-Core-File-L1-2-2.dll
 - KernelBase.dll
api_name:
 - SetFileApisToANSI
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# SetFileApisToANSI function


## -description


Causes the file I/O functions to use the ANSI character set code page for the current 
    process. This function is useful for 8-bit console input and output operations.


## -parameters






## -returns



This function does not return a value.




## -remarks



The file I/O functions whose code page is set by <b>SetFileApisToANSI</b> are those 
    functions exported by KERNEL32.DLL that accept or return a file name. 
    <b>SetFileApisToANSI</b> sets the code page per process, rather than per thread or per 
    computer.

The <b>SetFileApisToANSI</b> function complements the 
    <a href="https://msdn.microsoft.com/15f657d8-075a-4f0c-a653-73273ea62f5f">SetFileApisToOEM</a> function, which causes the same set 
    of file I/O functions to use the OEM character set code page.

The 8-bit console functions use the OEM code page by default. All other functions use the ANSI code page by 
    default. This means that strings returned by the console functions may not be processed correctly by other 
    functions, and vice versa. For example, if the 
    <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFileA</a> function returns a string that contains 
    certain extended ANSI characters, and the 8-bit console functions are set to use the OEM code page, then the 
    <a href="base.writeconsole">WriteConsoleA</a> function does not display the string 
    properly.

Use the <a href="https://msdn.microsoft.com/6bebe896-86d1-40b8-ab7f-0305ada71fdf">AreFileApisANSI</a> function to determine 
    which code page the set of file I/O functions is currently using. Use the 
    <a href="base.setconsolecp">SetConsoleCP</a> and 
    <a href="base.setconsoleoutputcp">SetConsoleOutputCP</a> functions to set the code page 
    for the 8-bit console functions.

To solve the problem of code page incompatibility, it is best to use Unicode for console applications. Console 
    applications that use Unicode are much more versatile than those that use 8-bit console functions. Barring that 
    solution, a console application can call the 
    <a href="https://msdn.microsoft.com/15f657d8-075a-4f0c-a653-73273ea62f5f">SetFileApisToOEM</a> function to cause the 
    set of file I/O functions to use OEM character set strings rather than ANSI character set strings. Use the 
    <b>SetFileApisToANSI</b> function to set those functions back to the ANSI code 
    page.

When dealing with command lines, a console application should obtain the command line in Unicode form and then 
    convert it to OEM form using the relevant character-to-OEM functions. Note also that the array in the 
    <i>argv</i> parameter of the command-line <b>main</b> function 
    contains ANSI character set strings in this case.

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




<a href="https://msdn.microsoft.com/6bebe896-86d1-40b8-ab7f-0305ada71fdf">AreFileApisANSI</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFileA</a>



<a href="base.setconsolecp">SetConsoleCP</a>



<a href="base.setconsoleoutputcp">SetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/15f657d8-075a-4f0c-a653-73273ea62f5f">SetFileApisToOEM</a>



<a href="base.writeconsole">WriteConsoleA</a>
 

 

