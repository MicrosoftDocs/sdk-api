---
UID: NF:winwlx.WlxShutdown
title: WlxShutdown function (winwlx.h)
description: Winlogon calls this function just before shutting down, allowing the GINA to perform any shutdown tasks, such as ejecting a smart card from a reader.
helpviewer_keywords: ["WLX_SAS_ACTION_SHUTDOWN","WLX_SAS_ACTION_SHUTDOWN_POWER_OFF","WLX_SAS_ACTION_SHUTDOWN_REBOOT","WlxShutdown","WlxShutdown function [Security]","_gina_wlxshutdown","security.wlxshutdown","winwlx/WlxShutdown"]
old-location: security\wlxshutdown.htm
tech.root: security
ms.assetid: dab8a93d-a0fe-4a29-9a29-ad64627050b7
ms.date: 12/05/2018
ms.keywords: WLX_SAS_ACTION_SHUTDOWN, WLX_SAS_ACTION_SHUTDOWN_POWER_OFF, WLX_SAS_ACTION_SHUTDOWN_REBOOT, WlxShutdown, WlxShutdown function [Security], _gina_wlxshutdown, security.wlxshutdown, winwlx/WlxShutdown
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlxShutdown
 - winwlx/WlxShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxShutdown
---

# WlxShutdown function


## -description

<p class="CCE_Message">[The WlxShutdown function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxShutdown</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function just before shutting down, allowing the GINA to perform any shutdown tasks, such as ejecting a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> from a <a href="/windows/desktop/SecGloss/r-gly">reader</a>.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

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

## -remarks

Winlogon calls <b>WlxShutdown</b> after the user has logged off and the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxlogoff">WlxLogoff</a> function has been called.

Before calling <b>WlxShutdown</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxlogoff">WlxLogoff</a>