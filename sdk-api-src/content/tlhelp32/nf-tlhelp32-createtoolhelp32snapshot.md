---
UID: NF:tlhelp32.CreateToolhelp32Snapshot
title: CreateToolhelp32Snapshot function (tlhelp32.h)
description: Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.
helpviewer_keywords: ["CreateToolhelp32Snapshot","CreateToolhelp32Snapshot function [ToolHelp]","TH32CS_INHERIT","TH32CS_SNAPALL","TH32CS_SNAPHEAPLIST","TH32CS_SNAPMODULE","TH32CS_SNAPMODULE32","TH32CS_SNAPPROCESS","TH32CS_SNAPTHREAD","_win32_createtoolhelp32snapshot","base.createtoolhelp32snapshot","tlhelp32/CreateToolhelp32Snapshot","toolhelp.createtoolhelp32snapshot"]
old-location: toolhelp\createtoolhelp32snapshot.htm
tech.root: ToolHelp
ms.assetid: df643c25-7558-424c-b187-b3f86ba51358
ms.date: 12/05/2018
ms.keywords: CreateToolhelp32Snapshot, CreateToolhelp32Snapshot function [ToolHelp], TH32CS_INHERIT, TH32CS_SNAPALL, TH32CS_SNAPHEAPLIST, TH32CS_SNAPMODULE, TH32CS_SNAPMODULE32, TH32CS_SNAPPROCESS, TH32CS_SNAPTHREAD, _win32_createtoolhelp32snapshot, base.createtoolhelp32snapshot, tlhelp32/CreateToolhelp32Snapshot, toolhelp.createtoolhelp32snapshot
req.header: tlhelp32.h
req.include-header: 
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
 - CreateToolhelp32Snapshot
 - tlhelp32/CreateToolhelp32Snapshot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-toolhelp-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
 - CreateToolhelp32Snapshot
---

# CreateToolhelp32Snapshot function


## -description

Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.

## -parameters

### -param dwFlags [in]

The portions of the system to be included in the snapshot. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TH32CS_INHERIT"></a><a id="th32cs_inherit"></a><dl>
<dt><b>TH32CS_INHERIT</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the snapshot handle is to be inheritable.

</td>
</tr>
<tr>
<td width="40%"><a id="TH32CS_SNAPALL"></a><a id="th32cs_snapall"></a><dl>
<dt><b>TH32CS_SNAPALL</b></dt>
</dl>
</td>
<td width="60%">
Includes all processes and threads in the system, plus the heaps and modules of the process specified in <i>th32ProcessID</i>. Equivalent to specifying the <b>TH32CS_SNAPHEAPLIST</b>,
                        <b>TH32CS_SNAPMODULE</b>, <b>TH32CS_SNAPPROCESS</b>, and
                        <b>TH32CS_SNAPTHREAD</b> values combined using an OR operation ('|').

</td>
</tr>
<tr>
<td width="40%"><a id="TH32CS_SNAPHEAPLIST"></a><a id="th32cs_snapheaplist"></a><dl>
<dt><b>TH32CS_SNAPHEAPLIST</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Includes all heaps of the process specified in <i>th32ProcessID</i> in the snapshot. To enumerate the heaps, see 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listfirst">Heap32ListFirst</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TH32CS_SNAPMODULE"></a><a id="th32cs_snapmodule"></a><dl>
<dt><b>TH32CS_SNAPMODULE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Includes all modules of the process specified in <i>th32ProcessID</i> in the snapshot. To enumerate the modules, see 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-module32first">Module32First</a>. If the function fails with <b>ERROR_BAD_LENGTH</b>, retry the function until it succeeds.

<b>64-bit Windows:  </b>Using this flag in a 32-bit process includes the 32-bit modules of the process specified in <i>th32ProcessID</i>, while using it in a 64-bit process includes the 64-bit modules. To include the 32-bit modules of the process specified in <i>th32ProcessID</i> from a 64-bit process, use the <b>TH32CS_SNAPMODULE32</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TH32CS_SNAPMODULE32"></a><a id="th32cs_snapmodule32"></a><dl>
<dt><b>TH32CS_SNAPMODULE32</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Includes all 32-bit modules of the process specified in <i>th32ProcessID</i> in the snapshot when called from a 64-bit process. This flag can be combined with <b>TH32CS_SNAPMODULE</b> or <b>TH32CS_SNAPALL</b>.  If the function fails with <b>ERROR_BAD_LENGTH</b>, retry the function until it succeeds.

</td>
</tr>
<tr>
<td width="40%"><a id="TH32CS_SNAPPROCESS"></a><a id="th32cs_snapprocess"></a><dl>
<dt><b>TH32CS_SNAPPROCESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Includes all processes in the system in the snapshot. To enumerate the processes, see 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-process32first">Process32First</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TH32CS_SNAPTHREAD"></a><a id="th32cs_snapthread"></a><dl>
<dt><b>TH32CS_SNAPTHREAD</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Includes all threads in the system in the snapshot. To enumerate the threads, see 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32first">Thread32First</a>.

To identify the threads that belong to a specific process, compare its process identifier to the <b>th32OwnerProcessID</b> member of the 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-threadentry32">THREADENTRY32</a> structure when enumerating the threads.

</td>
</tr>
</table>

### -param th32ProcessID [in]

The process identifier of the process to be included in the snapshot. This parameter can be zero to indicate the current process. This parameter is used when the <b>TH32CS_SNAPHEAPLIST</b>, <b>TH32CS_SNAPMODULE</b>, <b>TH32CS_SNAPMODULE32</b>, or <b>TH32CS_SNAPALL</b> value is specified. Otherwise, it is ignored and all processes are included in the snapshot.

If the specified process is the Idle process or one of the CSRSS processes, this function fails and the last error code is <b>ERROR_ACCESS_DENIED</b> because their access restrictions prevent user-level code from opening them.

If the specified process is a 64-bit process and the caller is a 32-bit process, this function fails and the last error code is <b>ERROR_PARTIAL_COPY</b> (299).

## -returns

If the function succeeds, it returns an open handle to the specified snapshot.

If the function fails, it returns <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes include <b>ERROR_BAD_LENGTH</b>.

## -remarks

The snapshot taken by this function is examined by the other tool help functions to provide their results. Access to the snapshot is read only. The snapshot handle acts as an object handle and is subject to the same rules regarding which processes and threads it is valid in.

To enumerate the heap or module states for all processes, specify <b>TH32CS_SNAPALL</b> and set <i>th32ProcessID</i> to zero. Then, for each additional process in the snapshot, call 
<b>CreateToolhelp32Snapshot</b> again, specifying its process identifier and the <b>TH32CS_SNAPHEAPLIST</b> or <b>TH32_SNAPMODULE</b> value.

When taking snapshots that include heaps and modules for a process other than the current process, the <b>CreateToolhelp32Snapshot</b> function can fail or return incorrect information for a variety of reasons. For example, if the loader data table in the target process is corrupted or not initialized, or if the module list changes during the function call as a result of DLLs being loaded or unloaded, the function might fail with <b>ERROR_BAD_LENGTH</b> or other error code. Ensure that the target process was not started in a suspended state,  and try calling the function again.  If the function fails with <b>ERROR_BAD_LENGTH</b> when called with <b>TH32CS_SNAPMODULE</b> or <b>TH32CS_SNAPMODULE32</b>,   call the function again until it succeeds. 

The <b>TH32CS_SNAPMODULE</b> and <b>TH32CS_SNAPMODULE32</b> flags do not retrieve handles for modules that were loaded with the <b>LOAD_LIBRARY_AS_DATAFILE</b> or similar flags. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>.

To destroy the snapshot, use the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

Note that you can use the <a href="/windows/desktop/api/winbase/nf-winbase-queryfullprocessimagenamea">QueryFullProcessImageName</a> function to retrieve the full name of an executable image for both 32- and 64-bit processes from a 32-bit process.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/taking-a-snapshot-and-viewing-processes">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listfirst">Heap32ListFirst</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-module32first">Module32First</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-process32first">Process32First</a>



<a href="/windows/desktop/ToolHelp/snapshots-of-the-system">Snapshots of the System</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32first">Thread32First</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>