---
UID: NF:winwlx.WlxWkstaLockedSAS
title: WlxWkstaLockedSAS function (winwlx.h)
description: Winlogon calls this function when it receives a secure attention sequence (SAS) and the workstation is locked.
helpviewer_keywords: ["WLX_SAS_TYPE_CTRL_ALT_DEL","WLX_SAS_TYPE_SC_INSERT","WLX_SAS_TYPE_SC_REMOVE","WLX_SAS_TYPE_TIMEOUT","WlxWkstaLockedSAS","WlxWkstaLockedSAS function [Security]","_gina_wlxwkstalockedsas","security.wlxwkstalockedsas","winwlx/WlxWkstaLockedSAS"]
old-location: security\wlxwkstalockedsas.htm
tech.root: security
ms.assetid: 7a9f8b00-857a-432e-bb49-2251504c46a0
ms.date: 12/05/2018
ms.keywords: WLX_SAS_TYPE_CTRL_ALT_DEL, WLX_SAS_TYPE_SC_INSERT, WLX_SAS_TYPE_SC_REMOVE, WLX_SAS_TYPE_TIMEOUT, WlxWkstaLockedSAS, WlxWkstaLockedSAS function [Security], _gina_wlxwkstalockedsas, security.wlxwkstalockedsas, winwlx/WlxWkstaLockedSAS
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
 - WlxWkstaLockedSAS
 - winwlx/WlxWkstaLockedSAS
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
 - WlxWkstaLockedSAS
---

# WlxWkstaLockedSAS function


## -description

The <b>WlxWkstaLockedSAS</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function when it receives a <a href="/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS) and the workstation is locked. The GINA should return a value that indicates the workstation is to remain locked, the workstation is to be unlocked, or the logged-on user is to be logged off (which leaves the workstation locked until the logoff is completed).
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param dwSasType [in]

Specifies the type of SAS that occurred. Values from zero to WLX_SAS_TYPE_MAX_MSFT_VALUE are reserved for standard Microsoft SAS types. GINA developers can use values greater than WLX_SAS_TYPE_MAX_MSFT_VALUE to define additional SAS types.

The following SAS types are predefined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_CTRL_ALT_DEL"></a><a id="wlx_sas_type_ctrl_alt_del"></a><dl>
<dt><b>WLX_SAS_TYPE_CTRL_ALT_DEL</b></dt>
</dl>
</td>
<td width="60%">
Indicates a user has typed the standard CTRL+ALT+DEL <a href="/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS).

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_INSERT"></a><a id="wlx_sas_type_sc_insert"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_INSERT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> has been inserted into a compatible device.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_REMOVE"></a><a id="wlx_sas_type_sc_remove"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_REMOVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a smart card has been removed from a compatible device.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_TIMEOUT"></a><a id="wlx_sas_type_timeout"></a><dl>
<dt><b>WLX_SAS_TYPE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that no user input was received within the specified time-out period.

</td>
</tr>
</table>

## -returns

The <b>WlxWkstaLockedSAS</b> function should return the following values.

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
Tells <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> to keep the workstation locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_FORCE_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
Tells Winlogon to forcibly log the user off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_LOGOFF</b></dt>
</dl>
</td>
<td width="60%">
Tells Winlogon to log the current user off.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_UNLOCK_WKSTA</b></dt>
</dl>
</td>
<td width="60%">
Tells Winlogon to unlock the workstation.

</td>
</tr>
</table>

## -remarks

Before calling <b>WlxWkstaLockedSAS</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>