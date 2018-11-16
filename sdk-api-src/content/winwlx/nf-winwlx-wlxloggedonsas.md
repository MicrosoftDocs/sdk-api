---
UID: NF:winwlx.WlxLoggedOnSAS
title: WlxLoggedOnSAS function
author: windows-sdk-content
description: Winlogon calls this function when it receives a secure attention sequence (SAS) event while the user is logged on and the workstation is not locked.
old-location: security\wlxloggedonsas.htm
tech.root: SecAuthN
ms.assetid: d60d1464-1948-444c-801a-dde17905091b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WLX_SAS_TYPE_CTRL_ALT_DEL, WLX_SAS_TYPE_SC_INSERT, WLX_SAS_TYPE_SC_REMOVE, WLX_SAS_TYPE_TIMEOUT, WlxLoggedOnSAS, WlxLoggedOnSAS function [Security], _gina_wlxloggedonsas, security.wlxloggedonsas, winwlx/WlxLoggedOnSAS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winwlx.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxLoggedOnSAS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WlxLoggedOnSAS
: 
---

# WlxLoggedOnSAS function


## -description


<p class="CCE_Message">[The WlxLoggedOnSAS function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxLoggedOnSAS</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function when it receives a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS) event while the user is logged on and the workstation is not locked.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


### -param dwSasType [in]

Specifies the type of SAS that occurred. Values from zero to WLX_SAS_TYPE_MAX_MSFT_VALUE are reserved to define standard Microsoft SAS types. GINA developers can define additional SAS types by using values greater than WLX_SAS_TYPE_MAX_MSFT_VALUE.

The following SAS types are predefined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_TIMEOUT"></a><a id="wlx_sas_type_timeout"></a><dl>
<dt><b>WLX_SAS_TYPE_TIMEOUT</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
Indicates that no user input was received within the specified time-out period.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_CTRL_ALT_DEL"></a><a id="wlx_sas_type_ctrl_alt_del"></a><dl>
<dt><b>WLX_SAS_TYPE_CTRL_ALT_DEL</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Indicates that a user has typed the standard CTRL+ALT+DEL <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS).

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_INSERT"></a><a id="wlx_sas_type_sc_insert"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_INSERT</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">
Indicates that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> has been inserted into a compatible device.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_REMOVE"></a><a id="wlx_sas_type_sc_remove"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_REMOVE</b></dt>
<dt>6 (0x6)</dt>
</dl>
</td>
<td width="60%">
Indicates that a smart card has been removed from a compatible device.

</td>
</tr>
</table>
 


### -param pReserved [in]

This parameter is reserved and must be set to <b>NULL</b>.


## -returns



The <b>WlxLoggedOnSAS</b> function should return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_NONE</b></dt>
</dl>
</td>
<td width="60%">
Returns to the default desktop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_LOCK_WKSTA</b></dt>
</dl>
</td>
<td width="60%">
Locks the workstation and waits for the next SAS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
Logs the user off the workstation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
Logs the user off and shuts down the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN_REBOOT</b></dt>
</dl>
</td>
<td width="60%">
Logs the user off, shuts down the computer, and then restarts the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN_POWER_OFF</b></dt>
</dl>
</td>
<td width="60%">
If hardware allows, logs the user off, shuts down the computer, and then turns off the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_PWD_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
Notifies network providers that the user changed their password. Obsolete GINA DLLs should call <a href="https://msdn.microsoft.com/53765f8f-50cb-40dd-888e-0e1ddbe76f7e">WlxChangePasswordNotify</a> whenever a password is changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_TASKLIST</b></dt>
</dl>
</td>
<td width="60%">
Invokes the task list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_FORCE_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
Forcibly logs off the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN_SLEEP</b></dt>
</dl>
</td>
<td width="60%">
Puts the computer in suspend mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN_SLEEP2</b></dt>
</dl>
</td>
<td width="60%">
Shuts down the system into an ACPI power-down state. If the computer is not an ACPI computer, this option will have no effect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN_HIBERNATE</b></dt>
</dl>
</td>
<td width="60%">
Shuts down the system into the hibernate mode. If the system was not configured for hibernation, this option will have no effect.

</td>
</tr>
</table>
 




## -remarks



Winlogon calls <b>WlxLoggedOnSAS</b> when the logged-on user wants to shut down, log out, or lock the workstation. The <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL can lock the workstation by returning WLX_SAS_ACTION_LOCK_WKSTA. When this value is returned, <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> locks the workstation and calls 
<a href="https://msdn.microsoft.com/7a9f8b00-857a-432e-bb49-2251504c46a0">WlxWkstaLockedSAS</a> the next time it receives an SAS.

Before calling <b>WlxLoggedOnSAS</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/7a9f8b00-857a-432e-bb49-2251504c46a0">WlxWkstaLockedSAS</a>
 

 

