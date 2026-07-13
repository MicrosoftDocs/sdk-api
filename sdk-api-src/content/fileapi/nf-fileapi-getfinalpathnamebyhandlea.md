---
UID: NF:fileapi.GetFinalPathNameByHandleA
title: GetFinalPathNameByHandleA function (fileapi.h)
description: Retrieves the final path for the specified file. (ANSI)
helpviewer_keywords: ["FILE_NAME_NORMALIZED", "FILE_NAME_OPENED", "GetFinalPathNameByHandleA", "VOLUME_NAME_DOS", "VOLUME_NAME_GUID", "VOLUME_NAME_NONE", "VOLUME_NAME_NT", "fileapi/GetFinalPathNameByHandleA"]
old-location: fs\getfinalpathnamebyhandle.htm
tech.root: fs
ms.assetid: 02783ba9-a8d7-482f-a8b1-7cac934cf476
ms.date: 12/05/2018
ms.keywords: FILE_NAME_NORMALIZED, FILE_NAME_OPENED, GetFinalPathNameByHandle, GetFinalPathNameByHandle function [Files], GetFinalPathNameByHandleA, GetFinalPathNameByHandleW, VOLUME_NAME_DOS, VOLUME_NAME_GUID, VOLUME_NAME_NONE, VOLUME_NAME_NT, fileapi/GetFinalPathNameByHandle, fileapi/GetFinalPathNameByHandleA, fileapi/GetFinalPathNameByHandleW, fs.getfinalpathnamebyhandle, fs.getfinalpathnamebyhandlew, winbase/GetFinalPathNameByHandle, winbase/GetFinalPathNameByHandleA, winbase/GetFinalPathNameByHandleW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFinalPathNameByHandleW (Unicode) and GetFinalPathNameByHandleA (ANSI)
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
 - GetFinalPathNameByHandleA
 - fileapi/GetFinalPathNameByHandleA
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
 - GetFinalPathNameByHandle
 - GetFinalPathNameByHandleA
 - GetFinalPathNameByHandleW
---

# GetFinalPathNameByHandleA function


## -description

Retrieves the final path for the specified file.

For more information about file and path names, see 
    <a href="/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

## -parameters

### -param hFile [in]

A handle to a file or directory.

### -param lpszFilePath [out]

A pointer to a buffer that receives the path of <i>hFile</i>.

### -param cchFilePath [in]

The size of <i>lpszFilePath</i>, in <b>TCHAR</b>s. This value must include a <b>NULL</b> termination character.

### -param dwFlags [in]

The type of result to return.  This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_NAME_NORMALIZED"></a><a id="file_name_normalized"></a><dl>
<dt><b>FILE_NAME_NORMALIZED</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Return the normalized drive name. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NAME_OPENED"></a><a id="file_name_opened"></a><dl>
<dt><b>FILE_NAME_OPENED</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Return the opened file name (not normalized).

</td>
</tr>
</table>
 

This parameter can also include one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VOLUME_NAME_DOS"></a><a id="volume_name_dos"></a><dl>
<dt><b>VOLUME_NAME_DOS</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Return the path with the drive letter. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="VOLUME_NAME_GUID"></a><a id="volume_name_guid"></a><dl>
<dt><b>VOLUME_NAME_GUID</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Return the path with a volume <b>GUID</b> path instead of the drive name.

</td>
</tr>
<tr>
<td width="40%"><a id="_VOLUME_NAME_NONE"></a><a id="_volume_name_none"></a><dl>
<dt><b> VOLUME_NAME_NONE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Return the path with no drive information.

</td>
</tr>
<tr>
<td width="40%"><a id="VOLUME_NAME_NT"></a><a id="volume_name_nt"></a><dl>
<dt><b>VOLUME_NAME_NT</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Return the path with the volume device path.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the length of the string received by 
       <i>lpszFilePath</i>, in <b>TCHAR</b>s. This value does not include the 
       size of the terminating null character.

<b>Windows Server 2008 and Windows Vista:  </b>For the ANSI version of this function, 
        <b>GetFinalPathNameByHandleA</b>, the return value 
        includes the size of the terminating null character.

If the function fails because <i>lpszFilePath</i> is too small to hold the string plus the 
       terminating null character, the return value is the required buffer size, in 
       <b>TCHAR</b>s. This value includes the size of the terminating null character.

If the function fails for any other reason, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Can be returned if you are searching for a drive letter and one does not exist.  For example, the handle 
         was opened on a drive that is not currently mounted, or if you create a volume and do not assign it a drive 
         letter. If a volume has no drive letter, you can use the volume <b>GUID</b> path to 
         identify it.

This return value can also be returned if you are searching for a volume <b>GUID</b> 
         path on a network share. Volume <b>GUID</b> paths are not created for network 
         shares.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid flags were specified for <i>dwFlags</i>.

</td>
</tr>
</table>

## -remarks

The Server Message Block (SMB) Protocol does not support queries for normalized paths. Consequently, when you call this function passing the handle of a file opened using SMB, and with the FILE_NAME_NORMALIZED flag, the function splits the path into its components and tries to query for the normalized name of each of those components in turn. If the user lacks access permission to any one of those components, then the function call fails with ERROR_ACCESS_DENIED.

> [!NOTE]
> Windows 10 version 1709 and later and Windows Server version 1709 and later support the **FileNormalizedNameInformation** information class via SMB. See the [MS-SMB2 specification] (/openspecs/windows_protocols/ms-smb2/a64e55aa-1152-48e4-8206-edd96444e7f7#Appendix_A_414) Appendix A, Section 3.3.5.20.1 for more information.

 A final path is the path that is returned when a path is fully resolved. For example, for a symbolic link 
     named "C:\tmp\mydir" that points to "D:\yourdir", the final path would be 
     "D:\yourdir".

The string that is returned by this function uses the "\\\\?\\" 
     syntax. For more information, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

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

The following example demonstrates the use of the 
     <b>GetFinalPathNameByHandle</b> function.


```cpp
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE MAX_PATH

void __cdecl _tmain(int argc, TCHAR *argv[])
{
    TCHAR Path[BUFSIZE];
    HANDLE hFile;
    DWORD dwRet;

    printf("\n");
    if( argc != 2 )
    {
        printf("ERROR:\tIncorrect number of arguments\n\n");
        printf("%s <file_name>\n", argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],               // file to open
                       GENERIC_READ,          // open for reading
                       FILE_SHARE_READ,       // share for reading
                       NULL,                  // default security
                       OPEN_EXISTING,         // existing file only
                       FILE_ATTRIBUTE_NORMAL, // normal file
                       NULL);                 // no attr. template

    if( hFile == INVALID_HANDLE_VALUE)
    {
        printf("Could not open file (error %d\n)", GetLastError());
        return;
    }

    dwRet = GetFinalPathNameByHandle( hFile, Path, BUFSIZE, VOLUME_NAME_NT );
    if(dwRet < BUFSIZE)
    {
        _tprintf(TEXT("\nThe final path is: %s\n"), Path);
    }
    else printf("\nThe required buffer size is %d.\n", dwRet);

    CloseHandle(hFile);
}

```






> [!NOTE]
> The fileapi.h header defines GetFinalPathNameByHandle as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>
