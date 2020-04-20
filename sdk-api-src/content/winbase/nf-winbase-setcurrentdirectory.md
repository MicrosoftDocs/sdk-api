---
UID: NF:winbase.SetCurrentDirectory
title: SetCurrentDirectory function (winbase.h)
description: Changes the current directory for the current process.helpviewer_keywords: ["SetCurrentDirectory","SetCurrentDirectory function [Files]","SetCurrentDirectoryA","SetCurrentDirectoryW","_win32_setcurrentdirectory","base.setcurrentdirectory","fs.setcurrentdirectory","winbase/SetCurrentDirectory","winbase/SetCurrentDirectoryA","winbase/SetCurrentDirectoryW"]
old-location: fs\setcurrentdirectory.htm
tech.root: FileIO
ms.assetid: 02dd0a2b-8072-4ce5-99b4-ffa6dcbd46cd
ms.date: 12/05/2018
ms.keywords: SetCurrentDirectory, SetCurrentDirectory function [Files], SetCurrentDirectoryA, SetCurrentDirectoryW, _win32_setcurrentdirectory, base.setcurrentdirectory, fs.setcurrentdirectory, winbase/SetCurrentDirectory, winbase/SetCurrentDirectoryA, winbase/SetCurrentDirectoryW
f1_keywords:
- winbase/SetCurrentDirectory
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetCurrentDirectoryW (Unicode) and SetCurrentDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessEnvironment-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-ProcessEnvironment-l1-2-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
api_name:
- SetCurrentDirectory
- SetCurrentDirectoryA
- SetCurrentDirectoryW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetCurrentDirectory function


## -description


Changes the current directory for the current process.


## -parameters




### -param lpPathName [in]

The path to the new current directory. This parameter may specify a relative path or a full path. In either case, the full path of the specified directory is calculated and stored as the current directory. 


For more information, see <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">File Names, Paths, and Namespaces</a>.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 

 The final character before the null character must be a backslash ('\'). If you do not specify the backslash, it will be added for you; therefore, specify <b>MAX_PATH</b>-2 characters for the path unless you  include the trailing backslash, in which case, specify <b>MAX_PATH</b>-1 characters for the path.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>SetCurrentDirectoryW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation. See the "Maximum Path Length Limitation" section of <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Each process has a single current directory made up of two parts:

<ul>
<li>A disk designator that is either a drive letter followed by a colon, or a server name and share name (\\<i>servername</i>\<i>sharename</i>)</li>
<li>A directory on the disk designator</li>
</ul>
Multithreaded applications and shared library code should not use the   
    <b>SetCurrentDirectory</b> function and should avoid using relative path names. The current directory state written by the <b>SetCurrentDirectory</b> function is stored as a global variable in each process, therefore multithreaded applications cannot reliably use this value without possible data corruption from other threads that may also be reading or setting this value. This limitation also applies to the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory">GetCurrentDirectory</a> and <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a> functions. The exception being when the application is guaranteed to be running in a single thread, for example parsing file names from the command line argument string in the main thread prior to creating any additional threads. Using relative path names in multithreaded applications or shared library code can yield unpredictable results and is not supported.

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
<a href="https://docs.microsoft.com/windows/desktop/FileIO/changing-the-current-directory">Changing the Current Directory</a>.
				

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory">GetCurrentDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>
 

 

