---
UID: NF:winsvc.NotifyBootConfigStatus
title: NotifyBootConfigStatus function (winsvc.h)
description: Reports the boot status to the service control manager. It is used by boot verification programs.
helpviewer_keywords: ["NotifyBootConfigStatus","NotifyBootConfigStatus function","_win32_notifybootconfigstatus","base.notifybootconfigstatus","winsvc/NotifyBootConfigStatus"]
old-location: base\notifybootconfigstatus.htm
tech.root: security
ms.assetid: 0b2b9cd0-f897-4681-9e99-5d0bed986112
ms.date: 12/05/2018
ms.keywords: NotifyBootConfigStatus, NotifyBootConfigStatus function, _win32_notifybootconfigstatus, base.notifybootconfigstatus, winsvc/NotifyBootConfigStatus
req.header: winsvc.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NotifyBootConfigStatus
 - winsvc/NotifyBootConfigStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-base-bootconfig-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - NotifyBootConfigStatus
---

# NotifyBootConfigStatus function


## -description

Reports the boot status to the service control manager. It is used by boot verification programs. This function can be called only by a process running in the LocalSystem or Administrator's account.

## -parameters

### -param BootAcceptable [in]

If the value is TRUE, the system saves the configuration as the last-known good configuration. If the value is FALSE, the system immediately reboots, using the previously saved last-known good configuration.

## -returns

If the <i>BootAcceptable</i> parameter is FALSE, the function does not return.

If the last-known good configuration was successfully saved, the return value is nonzero.

If an error occurs, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes may be set by the service control manager. Other error codes may be set by the registry functions that are called by the service control manager to set parameters in the configuration registry.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have permission to perform this operation. Only the system and members of the Administrator's group can do so.

</td>
</tr>
</table>

## -remarks

Saving the configuration of a running system with this function is an acceptable method for saving the last-known good configuration. If the boot configuration is unacceptable, use this function to reboot the system using the existing last-known good configuration.

This function call requires the caller's token to have permission to acquire the SC_MANAGER_MODIFY_BOOT_CONFIG access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

## -see-also

<a href="/windows/desktop/Services/automatically-starting-services">Automatically Starting Services</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>