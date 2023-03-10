---
UID: NF:winbase.SetProcessDEPPolicy
title: SetProcessDEPPolicy function (winbase.h)
description: Changes data execution prevention (DEP) and DEP-ATL thunk emulation settings for a 32-bit process.
helpviewer_keywords: ["PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION","PROCESS_DEP_ENABLE","SetProcessDEPPolicy","SetProcessDEPPolicy function","base.setprocessdeppolicy","winbase/SetProcessDEPPolicy"]
old-location: base\setprocessdeppolicy.htm
tech.root: base
ms.assetid: 17c9f522-fd64-4061-9212-8fc91cc96b18
ms.date: 12/05/2018
ms.keywords: PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION, PROCESS_DEP_ENABLE, SetProcessDEPPolicy, SetProcessDEPPolicy function, base.setprocessdeppolicy, winbase/SetProcessDEPPolicy
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - SetProcessDEPPolicy
 - winbase/SetProcessDEPPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
api_name:
 - SetProcessDEPPolicy
---

# SetProcessDEPPolicy function


## -description

Changes data execution prevention (DEP) and DEP-ATL thunk emulation settings for a 32-bit process.

## -parameters

### -param dwFlags [in]

A <b>DWORD</b> that can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
If the DEP system policy is OptIn or OptOut and DEP is enabled for the process, setting <i>dwFlags</i> to 0 disables DEP for the process.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_DEP_ENABLE"></a><a id="process_dep_enable"></a><dl>
<dt><b>PROCESS_DEP_ENABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enables DEP permanently on the current process. After DEP has been enabled for the process by setting <b>PROCESS_DEP_ENABLE</b>, it cannot be disabled for the life of the process. 

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION"></a><a id="process_dep_disable_atl_thunk_emulation"></a><dl>
<dt><b>PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Disables DEP-ATL thunk emulation for the current process, which prevents the system from intercepting NX faults that originate from the Active Template Library (ATL) thunk layer. For more information, see the Remarks section. This flag can be specified only with  <b>PROCESS_DEP_ENABLE</b>.


</td>
</tr>
</table>

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To retrieve error values defined for this function,  call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetProcessDEPPolicy</b>  function overrides the system DEP policy for the current process unless its DEP policy was specified at process creation. The system DEP policy setting must be OptIn or OptOut. If the system DEP policy is AlwaysOff or AlwaysOn, <b>SetProcessDEPPolicy</b> returns an error. After DEP is enabled for a process, subsequent calls to <b>SetProcessDEPPolicy</b> are ignored. 

DEP policy specified at process creation with the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">PROC_THREAD_ATTRIBUTE_MITIGATION_POLICY</a> attribute cannot be changed for the life of the process. In this case, calls to <b>SetProcessDEPPolicy</b> fail with <b>ERROR_ACCESS_DENIED</b>.

<b>SetProcessDEPPolicy</b> is supported for 32-bit processes only. If this function is called on a 64-bit process, it fails with <b>ERROR_NOT_SUPPORTED</b>.

Applications written to ATL 7.1 and earlier can attempt to execute code on pages marked as non-executable, which triggers an NX fault and terminates the application. DEP-ATL thunk emulation allows an application that would otherwise trigger an NX fault to run with DEP enabled. For information about ATL versions, see <a href="/previous-versions/visualstudio/visual-studio-2008/3z02ch3k(v=vs.90)">ATL and MFC Version Numbers</a>.

If DEP-ATL thunk emulation is enabled, the system intercepts NX faults, emulates the instructions, and handles the exceptions so the application can continue to run. If DEP-ATL thunk emulation is disabled by setting <b>PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION</b> for the process, NX faults are not intercepted, which is useful when testing applications for compatibility with DEP.

The following table summarizes the interactions between system DEP policy, DEP-ATL thunk emulation, and  <b>SetProcessDEPPolicy</b>.
To get the system DEP policy setting, use the <a href="/windows/desktop/api/winbase/nf-winbase-getsystemdeppolicy">GetSystemDEPPolicy</a> function.

<table>
<tr>
<th>System DEP policy</th>
<th>DEP behavior</th>
<th>DEP_ATL thunk emulation behavior</th>
<th><b>SetProcessDEPPolicy</b> behavior</th>
</tr>
<tr>
<td>
AlwaysOff

0

</td>
<td>
Disabled for the operating system and all processes.

</td>
<td>
Not applicable.

</td>
<td>
Returns an error.

</td>
</tr>
<tr>
<td>
AlwaysOn

1

</td>
<td>
Enabled for the operating system and all processes.

</td>
<td>
Disabled.

</td>
<td>
Returns an error.

</td>
</tr>
<tr>
<td>
OptIn

2

Default configuration for Windows client versions.

</td>
<td>
Enabled for the operating system and disabled for nonsystem processes. Administrators can  explicitly enable DEP for selected executable files.

</td>
<td>
Not applicable.

</td>
<td>
DEP can be enabled for the current process.

If DEP is enabled for the current process, DEP-ATL thunk emulation can be disabled for that process.

</td>
</tr>
<tr>
<td>
OptOut

3

Default configuration for Windows Server versions.

</td>
<td>
Enabled for the operating system and all processes. Administrators can explicitly disable DEP for selected executable files.

</td>
<td>
Enabled.

</td>
<td>
DEP can be disabled for the current process.

If DEP is disabled for the current process, DEP-ATL thunk emulation is automatically disabled for that process. 

</td>
</tr>
</table>
 

To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/Memory/data-execution-prevention">Data Execution Prevention</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getprocessdeppolicy">GetProcessDEPPolicy</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getsystemdeppolicy">GetSystemDEPPolicy</a>