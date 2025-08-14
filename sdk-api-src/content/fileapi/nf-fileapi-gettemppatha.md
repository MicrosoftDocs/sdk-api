---
UID: NF:fileapi.GetTempPathA
title: GetTempPathA function (fileapi.h)
description: Retrieves the path of the directory designated for temporary files. (ANSI)
helpviewer_keywords: ["GetTempPathA", "fileapi/GetTempPathA"]
old-location: fs\gettemppath.htm
tech.root: fs
ms.assetid: fb366f0d-df6b-44c2-92c9-b7a8e2583054
ms.date: 12/05/2018
ms.keywords: GetTempPath, GetTempPath function [Files], GetTempPathA, GetTempPathW, _win32_gettemppath, base.gettemppath, fileapi/GetTempPath, fileapi/GetTempPathA, fileapi/GetTempPathW, fs.gettemppath, winbase/GetTempPath, winbase/GetTempPathA, winbase/GetTempPathW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTempPathW (Unicode) and GetTempPathA (ANSI)
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
 - GetTempPathA
 - fileapi/GetTempPathA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetTempPath
 - GetTempPathA
 - GetTempPathW
---

# GetTempPathA function


## -description

Retrieves the path of the directory designated for temporary files.

 

## -parameters

### -param nBufferLength [in]

The size of the string buffer identified by <i>lpBuffer</i>, in 
      <b>TCHARs</b>.

### -param lpBuffer [out]

A pointer to a string buffer that receives the null-terminated string specifying the temporary file path. 
      The returned string ends with a backslash, for example, "C:\\TEMP\\".

## -returns

If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string copied to <i>lpBuffer</i>, not including the terminating null character. If the 
       return value is greater than <i>nBufferLength</i>, the return value is the length, in 
       <b>TCHARs</b>, of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The maximum possible return value is <b>MAX_PATH</b>+1 (261).

## -remarks

> [!NOTE]
> Apps should call [GetTempPath2](/windows/win32/api/fileapi/nf-fileapi-gettemppath2a) instead of **GetTempPath**. 

The <b>GetTempPath</b> function checks for the existence of 
    environment variables in the following order and uses the first path found:

<ol>
<li>The path specified by the TMP environment variable.</li>
<li>The path specified by the TEMP environment variable.</li>
<li>The path specified by the USERPROFILE environment variable.</li>
<li>The Windows directory.</li>
</ol>
Note that the function does not verify that the path exists, nor does it test to see if the current process has 
     any kind of access rights to the path. The <b>GetTempPath</b> 
     function returns the properly formatted string that specifies the fully qualified path based on the environment 
     variable search order as previously specified. The application should verify the existence of the path and 
     adequate access rights to the path prior to any use for file I/O operations.

Symbolic link behavior—If the path points to a symbolic link, the temp path name 
    maintains any symbolic links.

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
> The fileapi.h header defines GetTempPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-gettempfilenamea">GetTempFileName</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
