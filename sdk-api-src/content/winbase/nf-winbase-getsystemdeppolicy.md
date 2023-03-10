---
UID: NF:winbase.GetSystemDEPPolicy
title: GetSystemDEPPolicy function (winbase.h)
description: Gets the data execution prevention (DEP) policy setting for the system.
helpviewer_keywords: ["GetSystemDEPPolicy","GetSystemDEPPolicy function","base.getsystemdeppolicy","winbase/GetSystemDEPPolicy"]
old-location: base\getsystemdeppolicy.htm
tech.root: base
ms.assetid: 82cb1d4e-c0e5-4601-aa55-9171a106c286
ms.date: 12/05/2018
ms.keywords: GetSystemDEPPolicy, GetSystemDEPPolicy function, base.getsystemdeppolicy, winbase/GetSystemDEPPolicy
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
 - GetSystemDEPPolicy
 - winbase/GetSystemDEPPolicy
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
 - GetSystemDEPPolicy
---

# GetSystemDEPPolicy function


## -description

Gets the data execution prevention (DEP) policy setting for the system.



## -returns

This function returns a value of type <b>DEP_SYSTEM_POLICY_TYPE</b>, which can be one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AlwaysOff</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
DEP is disabled for all parts of the system, regardless of hardware support for DEP. The processor runs in PAE mode with 32-bit versions of Windows unless PAE is disabled in the boot configuration data. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AlwaysOn</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
DEP is enabled for all parts of the system. All processes always run with DEP enabled. DEP cannot be explicitly disabled for selected applications. System compatibility fixes are ignored. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OptIn</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
On systems with processors that are capable of hardware-enforced DEP, DEP is automatically enabled only for operating system components. This is the default setting for client versions of Windows. DEP can be explicitly enabled for selected applications or the current process. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OptOut</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
DEP is automatically enabled for operating system components and all processes. This is the default setting for Windows Server versions. DEP can be explicitly disabled for selected applications or the current process. System compatibility fixes for DEP are in effect. 

</td>
</tr>
</table>

## -remarks

The system-wide DEP policy is configured at boot time according to the policy setting in the boot configuration data.  To change the system-wide DEP policy setting, use the <a href="/windows-hardware/drivers/devtest/bcdedit--set">BCDEdit /set</a> command to set the <b>nx</b> boot entry option.

If the system DEP policy is OptIn or OptOut, DEP can be selectively enabled or disabled for the current process by calling the <a href="/windows/desktop/api/winbase/nf-winbase-setprocessdeppolicy">SetProcessDEPPolicy</a> function. This function works only for 32-bit processes.

A user with administrative privileges can disable DEP for selected applications by using the <b>System</b> Control Panel application. If the system DEP policy is OptOut, DEP is disabled for these applications.

The Application Compatibility Toolkit can be used to create a list of individual applications that are exempt from DEP. If the system DEP policy is OptOut, DEP is automatically disabled for applications on the list.

## -see-also

<a href="/windows/desktop/Memory/data-execution-prevention">Data Execution Prevention</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getprocessdeppolicy">GetProcessDEPPolicy</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getsystemdeppolicy">GetSystemDEPPolicy</a>
