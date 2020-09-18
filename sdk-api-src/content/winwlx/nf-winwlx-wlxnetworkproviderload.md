---
UID: NF:winwlx.WlxNetworkProviderLoad
title: WlxNetworkProviderLoad function (winwlx.h)
description: Winlogon calls this function to collect valid authentication and identification information.
helpviewer_keywords: ["WlxNetworkProviderLoad","WlxNetworkProviderLoad function [Security]","_gina_wlxnetworkproviderload","security.wlxnetworkproviderload","winwlx/WlxNetworkProviderLoad"]
old-location: security\wlxnetworkproviderload.htm
tech.root: security
ms.assetid: d9a39211-f876-46d8-9a7c-c6bb3ba9edfe
ms.date: 12/05/2018
ms.keywords: WlxNetworkProviderLoad, WlxNetworkProviderLoad function [Security], _gina_wlxnetworkproviderload, security.wlxnetworkproviderload, winwlx/WlxNetworkProviderLoad
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
 - WlxNetworkProviderLoad
 - winwlx/WlxNetworkProviderLoad
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
 - WlxNetworkProviderLoad
---

# WlxNetworkProviderLoad function


## -description

<p class="CCE_Message">[The WlxNetworkProviderLoad function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxNetworkProviderLoad</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function to collect valid authentication and identification information.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param pNprNotifyInfo [out]

Points to an 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_mpr_notify_info">WLX_MPR_NOTIFY_INFO</a> structure that contains domain, user name, and password information for the user. Winlogon will use this information to provide identification and authentication information to network providers. 




The GINA is not required to return password information. Any <b>NULL</b> fields within the structure will be ignored by Winlogon. Use <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> to allocate each string; Winlogon will free them when they are no longer needed.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Return <b>TRUE</b> if the user was authenticated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Return <b>FALSE</b> if the user was not authenticated.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>