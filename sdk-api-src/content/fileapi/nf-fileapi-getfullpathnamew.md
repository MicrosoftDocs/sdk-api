---
UID: NF:fileapi.GetFullPathNameW
title: GetFullPathNameW function
author: windows-sdk-content
description: Retrieves the full path and file name of the specified file.
old-location: fs\getfullpathname.htm
old-project: FileIO
ms.assetid: 4cf59ee3-4065-4096-a2b5-fbed20aa5caa
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetFullPathName, GetFullPathName function [Files], GetFullPathNameA, GetFullPathNameW, _win32_getfullpathname, base.getfullpathname, fileapi/GetFullPathName, fileapi/GetFullPathNameA, fileapi/GetFullPathNameW, fs.getfullpathname, winbase/GetFullPathName, winbase/GetFullPathNameA, winbase/GetFullPathNameW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFullPathNameW (Unicode) and GetFullPathNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l1-2-0.dll
-	API-MS-Win-Core-File-l1-2-1.dll
-	API-MS-Win-Core-File-l1-2-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	GetFullPathName
-	GetFullPathNameA
-	GetFullPathNameW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# GetFullPathNameW function


## -description


Retrieves the full path and file name of the specified file.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/63cbcec6-e9f0-4db3-bf2f-03a987000af1">GetFullPathNameTransacted</a> function.

For more information about file and path names, see 
    <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>.
<div class="alert"><b>Note</b>  The <b>GetFullPathName</b> function is not recommended for 
    multithreaded applications or shared library code. For more information, see the Remarks section.</div><div> </div>

## -parameters




### -param lpFileName [in]

The name of the  file.

This parameter can be a short (the 8.3 form) or long file name. This string can also be a share or volume 
       name.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function (<b>GetFullPathNameW</b>), and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, for the unicode version of this function (<b>GetFullPathNameW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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
    <a href="https://msdn.microsoft.com/8ce69033-b69b-438b-a27f-938dd327c8ec">GetLongPathName</a> or 
    <a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a> to convert to long or short path 
    names, respectively.

If the return value is greater than or equal to the value specified in 
    <i>nBufferLength</i>, you can call the function again with a buffer that is large enough to 
    hold the path. For an example of this case in addition to using zero-length buffer for dynamic allocation, see the 
    Example Code section.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
Multithreaded applications and shared library code should not use the 
    <b>GetFullPathName</b> function and should avoid using relative 
    path names. The current directory state written by the 
    <a href="https://msdn.microsoft.com/02dd0a2b-8072-4ce5-99b4-ffa6dcbd46cd">SetCurrentDirectory</a> function is stored as a global 
    variable in each process, therefore multithreaded applications cannot reliably use this value without possible 
    data corruption from other threads that may also be reading or setting this value. This limitation also applies 
    to the <b>SetCurrentDirectory</b> and 
    <a href="https://msdn.microsoft.com/1fbe6289-2ca8-4ca8-b004-ecf513f9b0bd">GetCurrentDirectory</a> functions. The exception being 
    when the application is guaranteed to be running in a single thread, for example parsing file names from the 
    command line argument string in the main thread prior to creating any additional threads. Using relative path 
    names in multithreaded applications or shared library code can yield unpredictable results and is not 
    supported.

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
     <a href="https://msdn.microsoft.com/8ce69033-b69b-438b-a27f-938dd327c8ec">GetLongPathName</a>, and 
     <a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>. For another example using dynamic 
     allocation, see <a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;tchar.h&gt;
#include &lt;stdio.h&gt;

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
        if (lppPart != NULL &amp;&amp; *lppPart != 0)
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/63cbcec6-e9f0-4db3-bf2f-03a987000af1">GetFullPathNameTransacted</a>



<a href="https://msdn.microsoft.com/8ce69033-b69b-438b-a27f-938dd327c8ec">GetLongPathName</a>



<a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>



<a href="https://msdn.microsoft.com/fb366f0d-df6b-44c2-92c9-b7a8e2583054">GetTempPath</a>



<a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a>
 

 

