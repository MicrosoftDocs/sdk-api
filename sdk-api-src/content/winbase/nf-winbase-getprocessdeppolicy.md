---
UID: NF:winbase.GetProcessDEPPolicy
title: GetProcessDEPPolicy function (winbase.h)
description: Gets the data execution prevention (DEP) and DEP-ATL thunk emulation settings for the specified 32-bit process.Windows XP with SP3:  Gets the DEP and DEP-ATL thunk emulation settings for the current process.
helpviewer_keywords: ["GetProcessDEPPolicy","GetProcessDEPPolicy function","PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION","PROCESS_DEP_ENABLE","base.getprocessdeppolicy","winbase/GetProcessDEPPolicy"]
old-location: base\getprocessdeppolicy.htm
tech.root: base
ms.assetid: adf15b9c-24f4-49ea-9283-0db5f3f13e65
ms.date: 12/05/2018
ms.keywords: GetProcessDEPPolicy, GetProcessDEPPolicy function, PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION, PROCESS_DEP_ENABLE, base.getprocessdeppolicy, winbase/GetProcessDEPPolicy
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
 - GetProcessDEPPolicy
 - winbase/GetProcessDEPPolicy
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
 - GetProcessDEPPolicy
---

# GetProcessDEPPolicy function


## -description

Gets the data execution prevention (DEP) and DEP-ATL thunk emulation settings for the specified 32-bit process.<b>Windows XP with SP3:  </b>Gets the DEP and DEP-ATL thunk emulation settings for the current process.

## -parameters

### -param hProcess [in]

A handle to the process. <b>PROCESS_QUERY_INFORMATION</b> privilege is required to get the DEP policy of a process. 

<b>Windows XP with SP3:  </b>The <i>hProcess</i> parameter is ignored.

### -param lpFlags [out]

A <b>DWORD</b> that receives one or more of the following flags.

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
DEP is disabled for the specified process.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_DEP_ENABLE"></a><a id="process_dep_enable"></a><dl>
<dt><b>PROCESS_DEP_ENABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
DEP is enabled for the specified process.  

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION"></a><a id="process_dep_disable_atl_thunk_emulation"></a><dl>
<dt><b>PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
DEP-ATL thunk emulation is disabled for the specified process. For information about DEP-ATL thunk emulation, see <a href="/windows/desktop/api/winbase/nf-winbase-setprocessdeppolicy">SetProcessDEPPolicy</a>.

</td>
</tr>
</table>

### -param lpPermanent [out]

<b>TRUE</b> if DEP is enabled or disabled permanently for the specified process; otherwise <b>FALSE</b>. If <i>lpPermanent</i> is <b>TRUE</b>, the current DEP setting persists for the life of the process and cannot be changed by calling <a href="/windows/desktop/api/winbase/nf-winbase-setprocessdeppolicy">SetProcessDEPPolicy</a>.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To retrieve error values defined for this function,  call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetProcessDEPPolicy</b> is supported for 32-bit processes only. If this function is called on a 64-bit process, it fails with <b>ERROR_NOT_SUPPORTED</b>.

To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/Memory/data-execution-prevention">Data Execution Prevention</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getsystemdeppolicy">GetSystemDEPPolicy</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setprocessdeppolicy">SetProcessDEPPolicy</a>