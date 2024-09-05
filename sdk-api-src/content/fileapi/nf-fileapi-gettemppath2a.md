---
UID: NF:fileapi.GetTempPath2A
title: GetTempPath2A
ms.date: 10/07/2020
ms.topic: language-reference
targetos: Windows
description: Retrieves the path of the directory designated for temporary files, based on the privileges of the calling process. (ANSI)
helpviewer_keywords: ["GetTempPath2A", "GetTempPath2A", "fileapi/GetTempPath2A"]
tech.root: fs
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: fileapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 19044
req.target-min-winversvr: Windows Server Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: GetTempPath2W (Unicode) and GetTempPath2A (ANSI)
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-4.dll
 - kernel32.dll
 - kernelbase.dll
api_name:
 - GetTempPath2A
f1_keywords:
 - GetTempPath2A
 - fileapi/GetTempPath2A
dev_langs:
 - c++
---

## -description

Retrieves the path of the directory designated for temporary files, based on the privileges of the calling process.

## -parameters

### -param BufferLength [in]

The size of the string buffer identified by <i>lpBuffer</i>, in 
      <b>TCHARs</b>.


### -param Buffer [out]

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

When calling this function from a process running as SYSTEM it will return the path C:\Windows\SystemTemp, which is inaccessible to non-SYSTEM processes. For non-SYSTEM processes, **GetTempPath2** will behave the same as [GetTempPath](/windows/win32/api/fileapi/nf-fileapi-gettemppatha). 

The <b>GetTempPath2</b> function checks for the existence of 
    environment variables in the following order and uses the first path found:

<ol>
<li>The path specified by the TMP environment variable.</li>
<li>The path specified by the TEMP environment variable.</li>
<li>The path specified by the USERPROFILE environment variable.</li>
<li>The Windows directory.</li>
</ol>
Note that the function does not verify that the path exists, nor does it test to see if the current process has 
     any kind of access rights to the path. The <b>GetTempPath2</b> 
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
> The fileapi.h header defines GetTempPath2 as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-gettempfilenamea">GetTempFileName</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>

## -see-also

