---
UID: NF:winbase.SetCurrentDirectory
title: SetCurrentDirectory function (winbase.h)
description: Changes the current directory for the current process.
helpviewer_keywords: ["SetCurrentDirectory","SetCurrentDirectory function [Files]","SetCurrentDirectoryA","SetCurrentDirectoryW","_win32_setcurrentdirectory","base.setcurrentdirectory","fs.setcurrentdirectory","winbase/SetCurrentDirectory","winbase/SetCurrentDirectoryA","winbase/SetCurrentDirectoryW"]
old-location: fs\setcurrentdirectory.htm
tech.root: fs
ms.assetid: 02dd0a2b-8072-4ce5-99b4-ffa6dcbd46cd
ms.date: 12/05/2018
ms.keywords: SetCurrentDirectory, SetCurrentDirectory function [Files], SetCurrentDirectoryA, SetCurrentDirectoryW, _win32_setcurrentdirectory, base.setcurrentdirectory, fs.setcurrentdirectory, winbase/SetCurrentDirectory, winbase/SetCurrentDirectoryA, winbase/SetCurrentDirectoryW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetCurrentDirectory
 - winbase/SetCurrentDirectory
dev_langs:
 - c++
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
---

# SetCurrentDirectory function

## -description

Changes the current directory for the current process.

## -parameters

### -param lpPathName [in]

The path to the new current directory. This parameter may specify a relative path or a full path. In either case, the full path of the specified directory is calculated and stored as the current directory.

For more info, see [Naming files, paths, and namespaces](/windows/win32/fileio/naming-a-file).
 
By default, the name is limited to **MAX_PATH** characters.

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt in to remove the **MAX_PATH** limitation. For details, see the *Maximum path length limitation* section of [Naming files, paths, and namespaces](/windows/win32/fileio/naming-a-file).

> [!IMPORTANT]
> Setting a current directory longer than **MAX_PATH** causes [CreateProcessW](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessw) to fail.

The final character before the null character must be a backslash ('\\'). If you don't specify the backslash, then it will be added for you. Therefore, specify **>MAX_PATH**-2 characters for the path unless you include the trailing backslash; in which case, specify **MAX_PATH**-1 characters for the path.

## -returns

If the function succeeds, then the return value is non-zero.

If the function fails, then the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

Each process has a single current directory made up of two parts:

<ul>
<li>A disk designator that is either a drive letter followed by a colon, or a server name and share name (&#92;&#92;<i>servername</i>&#92;<i>sharename</i>)</li>
<li>A directory on the disk designator</li>
</ul>

The current directory is shared by all threads of the process:
If one thread changes the current directory, it affects all threads
in the process.

Multithreaded applications and shared library code should avoid
calling the <b>SetCurrentDirectory</b> function due to the risk of
affecting relative path calculations being performed by other threads.
Conversely,

multithreaded applications and shared library code should avoid
using relative paths so that they are unaffected by changes to the
current directory performed by other threads.

> [!NOTE]
The current directory for a process is locked while the process is executing. That prevents the directory from being deleted, moved, or renamed.

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

## Examples

For an example, see <a href="/windows/desktop/FileIO/changing-the-current-directory">Changing the current directory</a>.

## -see-also

* <a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>
* <a href="/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory">GetCurrentDirectory</a>
* <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>
