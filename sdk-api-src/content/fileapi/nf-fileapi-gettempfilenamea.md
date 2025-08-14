---
UID: NF:fileapi.GetTempFileNameA
title: GetTempFileNameA function (fileapi.h)
description: Creates a name for a temporary file. If a unique file name is generated, an empty file is created and the handle to it is released; otherwise, only a file name is generated. (GetTempFileNameA)
helpviewer_keywords: ["GetTempFileNameA", "fileapi/GetTempFileNameA"]
old-location: fs\gettempfilename.htm
tech.root: fs
ms.assetid: 0a30055f-a3b9-439f-9304-40ee8a07b967
ms.date: 12/05/2018
ms.keywords: GetTempFileName, GetTempFileName function [Files], GetTempFileNameA, GetTempFileNameW, _win32_gettempfilename, base.gettempfilename, fileapi/GetTempFileName, fileapi/GetTempFileNameA, fileapi/GetTempFileNameW, fs.gettempfilename, winbase/GetTempFileName, winbase/GetTempFileNameA, winbase/GetTempFileNameW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTempFileNameW (Unicode) and GetTempFileNameA (ANSI)
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
 - GetTempFileNameA
 - fileapi/GetTempFileNameA
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
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetTempFileName
 - GetTempFileNameA
 - GetTempFileNameW
---

# GetTempFileNameA function


## -description

Creates a name for a temporary file. If a unique file name is generated, an empty file is created and 
    the handle to it is released; otherwise, only a file name is generated.

## -parameters

### -param lpPathName [in]

The directory path for the file name. Applications typically specify a period (.) for the current directory 
       or the result of the <a href="/windows/desktop/api/fileapi/nf-fileapi-gettemppath2a">GetTempPath2</a> function. The string 
       cannot be longer than <b>MAX_PATH</b>–14 characters or
       <b>GetTempFileName</b> will fail. If this parameter is 
       <b>NULL</b>, the function fails.

### -param lpPrefixString [in]

The null-terminated prefix string. The function uses up to the first three characters of this string as the 
       prefix of the file name. This string must consist of characters in the OEM-defined character set.

### -param uUnique [in]

An unsigned integer to be used in creating the temporary file name. For more information, see Remarks.

If <i>uUnique</i> is zero, the function attempts to form a unique file name using the 
       current system time. If the file already exists, the number is increased by one and the functions tests if this 
       file already exists. This continues until a unique filename is found; the function creates a file by that name 
       and closes it.  Note that the function does not attempt  to verify the uniqueness of the file name when 
       <i>uUnique</i> is nonzero.

### -param lpTempFileName [out]

A pointer to the buffer that receives the temporary file name. This buffer should be 
       <b>MAX_PATH</b> characters to accommodate the path plus the terminating null character.

## -returns

If the function succeeds, the return value specifies the unique numeric value used in the temporary file 
       name. If the <i>uUnique</i> parameter is nonzero, the return value specifies that same 
       number.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


The following is a possible return value.



<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The length of the string pointed to by the <i>lpPathName</i> parameter is more than 
         <b>MAX_PATH</b>–14 characters.

</td>
</tr>
</table>

## -remarks

The <b>GetTempFileName</b> function creates a temporary 
    file name of the following form:

<i>&lt;path&gt;</i>&#92;<i>&lt;pre&gt;</i><i>&lt;uuuu&gt;</i>.TMP

The following table describes the file name syntax.

<table>
<tr>
<th>Component</th>
<th>Meaning</th>
</tr>
<tr>
<td><i>&lt;path&gt;</i></td>
<td>Path specified by the <i>lpPathName</i> parameter</td>
</tr>
<tr>
<td><i>&lt;pre&gt;</i></td>
<td>First three letters of the <i>lpPrefixString</i> string</td>
</tr>
<tr>
<td><i>&lt;uuuu&gt;</i></td>
<td>Hexadecimal value of <i>uUnique</i></td>
</tr>
</table>
 

If <i>uUnique</i> is zero, 
    <b>GetTempFileName</b> creates an empty file and closes it. If 
    <i>uUnique</i> is not zero, you must create the file yourself. Only a file name is created, 
    because <b>GetTempFileName</b> is not able to guarantee that 
    the file name is unique.

Only the lower 16 bits of the <i>uUnique</i> parameter are used. This limits 
    <b>GetTempFileName</b> to a maximum of 65,535 unique file names 
    if the <i>lpPathName</i> and <i>lpPrefixString</i> parameters remain the 
    same.

Due to the algorithm used to generate file names, 
    <b>GetTempFileName</b> can perform poorly when creating a large 
    number of files with the same prefix. In such cases, it is recommended that you construct unique file names based 
    on <b>GUID</b>s.

Temporary files whose names have been created by this function are not automatically deleted. To delete these 
    files call <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>.

To avoid problems resulting when converting an ANSI string, an application should call the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function to create a temporary file.

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
 


#### Examples

For an example, see 
     <a href="/windows/desktop/FileIO/creating-and-using-a-temporary-file">Creating and Using a Temporary File</a>.

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines GetTempFileName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-gettemppath2a">GetTempPath2</a>



<a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>
