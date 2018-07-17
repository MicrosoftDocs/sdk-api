---
UID: NF:winwlx.WlxShutdown
title: WlxShutdown function
author: windows-sdk-content
description: Winlogon calls this function just before shutting down, allowing the GINA to perform any shutdown tasks, such as ejecting a smart card from a reader.
old-location: security\wlxshutdown.htm
old-project: secauthn
ms.assetid: dab8a93d-a0fe-4a29-9a29-ad64627050b7
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WLX_SAS_ACTION_SHUTDOWN, WLX_SAS_ACTION_SHUTDOWN_POWER_OFF, WLX_SAS_ACTION_SHUTDOWN_REBOOT, WlxShutdown, WlxShutdown function [Security], _gina_wlxshutdown, security.wlxshutdown, winwlx/WlxShutdown
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ICONINFOEXW, *PICONINFOEXW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxShutdown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlxShutdown function


## -description


<p class="CCE_Message">[The WlxShutdown function is no longer available for use as of Windows Server 2008 and Windows Vista.]


			The <b>WlxShutdown</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> calls this function just before shutting down, allowing the GINA to perform any shutdown tasks, such as ejecting a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> from a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


### -param ShutdownType [in]

Specifies the type of shutdown. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_ACTION_SHUTDOWN"></a><a id="wlx_sas_action_shutdown"></a><dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">
Logs the user off and shuts down the computer.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_ACTION_SHUTDOWN_REBOOT"></a><a id="wlx_sas_action_shutdown_reboot"></a><dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN_REBOOT</b></dt>
<dt>11 (0xB)</dt>
</dl>
</td>
<td width="60%">
Shuts down and restarts the computer.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_ACTION_SHUTDOWN_POWER_OFF"></a><a id="wlx_sas_action_shutdown_power_off"></a><dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN_POWER_OFF</b></dt>
<dt>10 (0xA)</dt>
</dl>
</td>
<td width="60%">
Shuts down and turns off the computer, if the hardware allows.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



Winlogon calls <b>WlxShutdown</b> after the user has logged off and the 
<a href="https://msdn.microsoft.com/bbeafd41-fe01-497d-8514-a6c088a11d73">WlxLogoff</a> function has been called.

Before calling <b>WlxShutdown</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/bbeafd41-fe01-497d-8514-a6c088a11d73">WlxLogoff</a>
 

 

