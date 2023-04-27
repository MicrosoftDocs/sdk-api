---
UID: NF:cfgmgr32.CM_WaitNoPendingInstallEvents
title: CM_WaitNoPendingInstallEvents function (cfgmgr32.h)
description: The CMP_WaitNoPendingInstallEvents (CM_WaitNoPendingInstallEvents) function waits until there are no pending device installation activities for the PnP manager to perform.
helpviewer_keywords: ["CMP_WaitNoPendingInstallEvents","CM_WaitNoPendingInstallEvents","CM_WaitNoPendingInstallEvents function [Device and Driver Installation]","cfgmgr32/CM_WaitNoPendingInstallEvents","cfgmgrfn_096076fd-3ea8-42cb-9b51-ea551bde863d.xml","devinst.cmp_waitnopendinginstallevents"]
old-location: devinst\cmp_waitnopendinginstallevents.htm
tech.root: devinst
ms.assetid: 5be4c315-0e47-44ec-970c-855f302b355c
ms.date: 12/05/2018
ms.keywords: CMP_WaitNoPendingInstallEvents, CM_WaitNoPendingInstallEvents, CM_WaitNoPendingInstallEvents function [Device and Driver Installation], cfgmgr32/CM_WaitNoPendingInstallEvents, cfgmgrfn_096076fd-3ea8-42cb-9b51-ea551bde863d.xml, devinst.cmp_waitnopendinginstallevents
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_WaitNoPendingInstallEvents
 - cfgmgr32/CM_WaitNoPendingInstallEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
 - setupapi.dll
api_name:
 - CM_WaitNoPendingInstallEvents
---

# CM_WaitNoPendingInstallEvents function


## -description

The <b>CMP_WaitNoPendingInstallEvents</b> (CM_WaitNoPendingInstallEvents) function waits until there are no pending device installation activities for the PnP manager to perform.

## -parameters

### -param dwTimeout [in]

Specifies a time-out interval, in milliseconds. 

<ul>
<li>
If <i>dwTimeout</i> is set to zero, the function tests whether there are pending installation events and returns immediately.

</li>
<li>
If <i>dwTimeout</i> is set to INFINITE (defined in <i>Winbase.h</i>), the function's time-out interval never elapses.

</li>
<li>
For all other <i>dwTimeout</i> values, the function returns when the specified interval elapses, even if there are still pending installation events.

</li>
</ul>

## -returns

The function returns one of the following values (defined in <i>Winbase.h</i>):

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_OBJECT_0</b></dt>
</dl>
</td>
<td width="60%">
There are no pending installation activities.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out interval elapsed, and installation activities are still pending.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function failed. Call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for additional error information.

</td>
</tr>
</table>

## -remarks

The function waits for an internal event object, which the PnP manager sets when it determines that no installation activities are pending.

If a non-zero time-out value is specified, then <b>CMP_WaitNoPendingInstallEvents</b> will return either when no installation events are pending or when the time-out period has expired, whichever comes first. 

New installation events can occur at any time. This function just indicates that there are no pending installation activities at the moment it is called.

This function is typically used by <a href="/windows-hardware/drivers/">device installation applications</a>. For more information, see <a href="/windows-hardware/drivers/install/writing-a-device-installation-application">Writing a Device Installation Application</a>.

Do not call this function while processing any events inside of a system-initiated callback function that is expected to return within a short amount of time.  This includes service startup (for example in the <b>ServiceMain</b> callback function) or while processing any control in the service handler (for example, the <b>Handler</b> callback function), or from installation components such as class-installers or co-installers.

For Windows XP (with no service pack installed), this function must be called from <a href="/windows-hardware/drivers/">session zero</a>, with administrator privileges. For Windows XP with Service Pack 1 (SP1) and later versions of Windows, the function can be called from any session, and administrator privileges are not required.

## -see-also


[CM_WaitNoPendingInstallEvents](/windows/win32/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents)

[How a Device Installation Application checks for in-progress device installations](/windows-hardware/drivers/install/checking-for-in-progress-installations)
