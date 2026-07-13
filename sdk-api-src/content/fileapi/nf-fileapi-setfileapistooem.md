---
UID: NF:fileapi.SetFileApisToOEM
title: SetFileApisToOEM function (fileapi.h)
description: Causes the file I/O functions for the process to use the OEM character set code page.
helpviewer_keywords: ["SetFileApisToOEM","SetFileApisToOEM function [Files]","_win32_setfileapistooem","base.setfileapistooem","fileapi/SetFileApisToOEM","fs.setfileapistooem"]
old-location: fs\setfileapistooem.htm
tech.root: fs
ms.assetid: 15f657d8-075a-4f0c-a653-73273ea62f5f
ms.date: 12/05/2018
ms.keywords: SetFileApisToOEM, SetFileApisToOEM function [Files], _win32_setfileapistooem, base.setfileapistooem, fileapi/SetFileApisToOEM, fs.setfileapistooem
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
 - SetFileApisToOEM
 - fileapi/SetFileApisToOEM
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
 - API-Ms-Win-Core-File-L1-2-2.dll
 - KernelBase.dll
api_name:
 - SetFileApisToOEM
---

# SetFileApisToOEM function


## -description

Causes the file I/O functions for the process to use the OEM character set code page. This 
    function is useful for 8-bit console input and output operations.



## -remarks

The file I/O functions whose code page is set by <b>SetFileApisToOEM</b> are those 
    functions exported by KERNEL32.DLL that accept or return a file name. 
    <b>SetFileApisToOEM</b> sets the code page per process, rather than per thread or per 
    computer.

The <b>SetFileApisToOEM</b> function is complemented by the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi">SetFileApisToANSI</a> function, which causes the same 
     set of file I/O functions to use the ANSI character set code page.

The 8-bit console functions use the OEM code page by default. All other functions use the ANSI code page by 
    default. This means that strings returned by the console functions may not be processed correctly by other 
    functions, and vice versa. For example, if the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFileA</a> function returns a string that contains 
    certain extended ANSI characters, and the 8-bit console functions are set to use the OEM code page, then the 
    <a href="/windows/console/writeconsole">WriteConsoleA</a> function will not display the string 
    properly.

Use the <a href="/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi">AreFileApisANSI</a> function to determine 
    which code page the set of file I/O functions is currently using. Use the 
    <a href="/windows/console/setconsolecp">SetConsoleCP</a> and 
    <a href="/windows/console/setconsoleoutputcp">SetConsoleOutputCP</a> functions to set the code page 
    for the 8-bit console functions.

To solve the problem of code page incompatibility, it is best to use Unicode for console applications. Console 
    applications that use Unicode are much more versatile than those that use 8-bit console functions. Barring that 
    solution, a console application can call the <b>SetFileApisToOEM</b> function to cause 
    the set of file I/O functions to use OEM character set strings rather than ANSI character set strings. Use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi">SetFileApisToANSI</a> function to set those functions 
    back to the ANSI code page.

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

<a href="/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi">AreFileApisANSI</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFileA</a>



<a href="/windows/console/setconsolecp">SetConsoleCP</a>



<a href="/windows/console/setconsoleoutputcp">SetConsoleOutputCP</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi">SetFileApisToANSI</a>



<a href="/windows/console/writeconsole">WriteConsoleA</a>
