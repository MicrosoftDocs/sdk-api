---
UID: NC:winwlx.PWLX_SAS_NOTIFY
title: PWLX_SAS_NOTIFY (winwlx.h)
description: Called by GINA to notify Winlogon of a secure attention sequence (SAS) event.
helpviewer_keywords: ["PWLX_SAS_NOTIFY","PWLX_SAS_NOTIFY callback","WLX_SAS_TYPE_CTRL_ALT_DEL","WlxSasNotify","WlxSasNotify callback function [Security]","_gina_wlxsasnotify","security.wlxsasnotify","winwlx/WlxSasNotify"]
old-location: security\wlxsasnotify.htm
tech.root: security
ms.assetid: 534afdf8-6809-413a-ac5c-23978f2b288a
ms.date: 12/05/2018
ms.keywords: PWLX_SAS_NOTIFY, PWLX_SAS_NOTIFY callback, WLX_SAS_TYPE_CTRL_ALT_DEL, WlxSasNotify, WlxSasNotify callback function [Security], _gina_wlxsasnotify, security.wlxsasnotify, winwlx/WlxSasNotify
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
 - PWLX_SAS_NOTIFY
 - winwlx/PWLX_SAS_NOTIFY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxSasNotify
---

# PWLX_SAS_NOTIFY callback function


## -description

<p class="CCE_Message">[The WlxSasNotify function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to notify <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> of a <a href="/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS) event.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param dwSasType [in]

Specifies the type of SAS that occurred. 




Values from zero to WLX_SAS_TYPE_MAX_MSFT_VALUE are reserved to define standard Microsoft SAS types. GINA developers can use values greater than WLX_SAS_TYPE_MAX_MSFT_VALUE to define additional SAS types.

The following values are predefined.

This value will be delivered to one of the GINA SAS service routines called by Winlogon (<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedoutsas">WlxLoggedOutSAS</a>, 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedonsas">WlxLoggedOnSAS</a>, or 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxwkstalockedsas">WlxWkstaLockedSAS</a>).

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
Indicates that the user has typed the CTRL+ALT+DEL SAS.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedonsas">WlxLoggedOnSAS</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedoutsas">WlxLoggedOutSAS</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxwkstalockedsas">WlxWkstaLockedSAS</a>