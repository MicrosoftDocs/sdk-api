---
UID: NC:winwlx.PWLX_SET_OPTION
title: PWLX_SET_OPTION (winwlx.h)
description: Called by GINA to set the value of an option.
helpviewer_keywords: ["PWLX_SET_OPTION","PWLX_SET_OPTION callback","WlxSetOption","WlxSetOption callback function [Security]","_gina_wlxsetoption","security.wlxsetoption","winwlx/WlxSetOption"]
old-location: security\wlxsetoption.htm
tech.root: security
ms.assetid: 59f775dd-b3ed-4a57-bec7-fa6ddf267401
ms.date: 12/05/2018
ms.keywords: PWLX_SET_OPTION, PWLX_SET_OPTION callback, WlxSetOption, WlxSetOption callback function [Security], _gina_wlxsetoption, security.wlxsetoption, winwlx/WlxSetOption
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
 - PWLX_SET_OPTION
 - winwlx/PWLX_SET_OPTION
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
 - WlxSetOption
---

# PWLX_SET_OPTION callback function


## -description

<p class="CCE_Message">[The WlxSetOption function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to set the value of an option.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param Option [in]

Specifies one of the following options:

### -param Value [in]

Specifies a new value for the option.

### -param OldValue [out]

On return, pointer to the old value the option was set to.

## -returns

The <b>WlxSetOption</b> function returns one of the following values.

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
The option was set to the value specified in the <i>Value</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Winlogon did not set <i>Option</i> to <i>Value</i>.

</td>
</tr>
</table>

## -remarks

In order to access this function, the GINA DLL must use the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a> structure and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call.

Use 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_get_option">WlxGetOption</a> to retrieve the current value of an option.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_get_option">WlxGetOption</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>
