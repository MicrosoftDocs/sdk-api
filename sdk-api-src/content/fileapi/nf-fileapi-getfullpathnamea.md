---
UID: NF:fileapi.GetFullPathNameA
title: GetFullPathNameA function (fileapi.h)
description: Retrieves the full path and file name of the specified file. (ANSI)
helpviewer_keywords: ["GetFullPathNameA", "fileapi/GetFullPathNameA"]
old-location: fs\getfullpathname.htm
tech.root: fs
ms.assetid: 4cf59ee3-4065-4096-a2b5-fbed20aa5caa
ms.date: 12/05/2018
ms.keywords: GetFullPathName, GetFullPathName function [Files], GetFullPathNameA, GetFullPathNameW, _win32_getfullpathname, base.getfullpathname, fileapi/GetFullPathName, fileapi/GetFullPathNameA, fileapi/GetFullPathNameW, fs.getfullpathname, winbase/GetFullPathName, winbase/GetFullPathNameA, winbase/GetFullPathNameW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFullPathNameW (Unicode) and GetFullPathNameA (ANSI)
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
 - GetFullPathNameA
 - fileapi/GetFullPathNameA
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
 - GetFullPathName
 - GetFullPathNameA
 - GetFullPathNameW
---

# GetFullPathNameA function


## -description

Retrieves the full path and file name of the specified file.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfullpathnametransacteda">GetFullPathNameTransacted</a> function.

For more information about file and path names, see 
    <a href="/windows/desktop/FileIO/naming-a-file">File Names, Paths, and Namespaces</a>.
<div class="alert"><b>Note</b> See the Remarks section for discussion of
    the use of relative paths with the <b>GetFullPathName</b> function
    in multithreaded applications or shared library code.</div>

## -parameters

### -param lpFileName [in]

The name of the  file.

This parameter can be a short (the 8.3 form) or long file name. This string can also be a share or volume 
       name.


### -param nBufferLength [in]

The size of the buffer to receive the null-terminated string for the drive and path, in 
      <b>TCHARs</b>.

### -param lpBuffer [out]

A pointer to a buffer that receives the null-terminated string for the  drive and path.

### -param lpFilePart [out]

A pointer to a buffer that receives the address (within <i>lpBuffer</i>) of the final 
      file name component in the path. 

This parameter can be  <b>NULL</b>.

If <i>lpBuffer</i> 
      refers to a directory and not a file, <i>lpFilePart</i> receives zero.

## -returns

If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string copied to <i>lpBuffer</i>, not including the terminating null character.

If the <i>lpBuffer</i> buffer is too small to contain the path, the return value is the 
       size, in <b>TCHARs</b>, of the buffer that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetFullPathName</b> merges the name of the current drive 
    and directory with a specified file name to determine the full path and file name of a specified file. It also 
    calculates the address of the file name portion of the full path and file name.

This function does not verify that the resulting path and file name are valid, or that they see an existing 
    file on the associated volume.

Note that the <i>lpFilePart</i> parameter does not 
    require string buffer space, but only enough for a single address. This is because it simply returns an address 
    within the buffer that already exists for <i>lpBuffer</i>.

Share and volume names are 
    valid input for <i>lpFileName</i>. For example, the following list identities the returned path 
    and file names if test-2 is a remote computer and U: is a network mapped drive whose current directory is the root of the volume:

<ul>
<li>If you specify "\\test-2\q$\lh" the path returned is 
      "\\test-2\q$\lh"</li>
<li>If you specify "\\?\UNC\test-2\q$\lh" the path returned is 
      "\\?\UNC\test-2\q$\lh"</li>
<li>If you specify "U:" the path returned is the current directory on the 
      "U:\" drive</li>
</ul>
<b>GetFullPathName</b> does not convert the specified file 
    name, <i>lpFileName</i>. If the specified file name exists, you can use 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getlongpathnamea">GetLongPathName</a> or 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a> to convert to long or short path 
    names, respectively.

If the return value is greater than or equal to the value specified in 
    <i>nBufferLength</i>, you can call the function again with a buffer that is large enough to 
    hold the path. For an example of this case in addition to using zero-length buffer for dynamic allocation, see the 
    Example Code section.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>

Relative paths passed to the <b>GetFullPathName</b> function are
interpreted as relative to the process's current directory.
The current directory state written by the
<a href="/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory">SetCurrentDirectory</a>
function is global to the process and can be changed by any thread at any time.
Applications should be aware that
consecutive calls to the <b>GetFullPathName</b> function with a relative path
may produce different results if the current directory changes between the two calls.

To avoid problems caused by inconsistent results,
multithreaded applications and shared library code should avoid using relative paths.
If a relative path is received, it should be consumed exactly once,
either by passing the relative path directly to a function like <b>CreateFile</b>,
or by converting it to an absolute path and using the absolute path
from that point forward.

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

The following C++ example shows a basic use of 
     <b>GetFullPathName</b>, 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-getlongpathnamea">GetLongPathName</a>, and 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a>. For another example using dynamic 
     allocation, see <a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a>.


```cpp
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define LONG_DIR_NAME TEXT("c:\\longdirectoryname")

void _tmain(int argc, TCHAR *argv[])
{
    DWORD  retval=0;
    BOOL   success; 
    TCHAR  buffer[BUFSIZE]=TEXT(""); 
    TCHAR  buf[BUFSIZE]=TEXT(""); 
    TCHAR** lppPart={NULL};

   if( argc != 2 )
   {
      _tprintf(TEXT("Usage: %s [file]\n"), argv[0]);
      return;
   }

// Retrieve the full path name for a file. 
// The file does not need to exist.

    retval = GetFullPathName(argv[1],
                 BUFSIZE,
                 buffer,
                 lppPart);
    
    if (retval == 0) 
    {
        // Handle an error condition.
        printf ("GetFullPathName failed (%d)\n", GetLastError());
        return;
    }
    else 
    {
        _tprintf(TEXT("The full path name is:  %s\n"), buffer);
        if (lppPart != NULL && *lppPart != 0)
        {
            _tprintf(TEXT("The final component in the path name is:  %s\n"), *lppPart);
        }
    }


// Create a long directory name for use with the next two examples.

    success = CreateDirectory(LONG_DIR_NAME,
                              NULL);

    if (!success)
    {
        // Handle an error condition.
        printf ("CreateDirectory failed (%d)\n", GetLastError());
        return;
    }


// Retrieve the short path name.  

    retval = GetShortPathName(LONG_DIR_NAME,
                  buf,
                  BUFSIZE);

    if (retval == 0) 
    {
        // Handle an error condition.
         printf ("GetShortPathName failed (%d)\n", GetLastError());
         return;
    }
    else _tprintf(TEXT("The short name for %s is %s\n"), 
                  LONG_DIR_NAME, buf);


// Retrieve the long path name.  

    retval = GetLongPathName(buf,
              buffer,
              BUFSIZE);

    if (retval == 0) 
    {
        // Handle an error condition.
         printf ("GetLongPathName failed (%d)\n", GetLastError());
         return;
    }
    else _tprintf(TEXT("The long name for %s is %s\n"), buf, buffer);

// Clean up the directory.

    success = RemoveDirectory(LONG_DIR_NAME);
    if (!success)
    {
        // Handle an error condition.
        printf ("RemoveDirectory failed (%d)\n", GetLastError());
        return;
    }
}

```






> [!NOTE]
> The fileapi.h header defines GetFullPathName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfullpathnametransacteda">GetFullPathNameTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getlongpathnamea">GetLongPathName</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getshortpathnamew">GetShortPathName</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-gettemppatha">GetTempPath</a>



<a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a>
