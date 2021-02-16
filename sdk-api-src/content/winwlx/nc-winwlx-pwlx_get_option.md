---
UID: NC:winwlx.PWLX_GET_OPTION
title: PWLX_GET_OPTION (winwlx.h)
description: Called by GINA to retrieve the current value of an option.
helpviewer_keywords: ["PWLX_GET_OPTION","PWLX_GET_OPTION callback","WlxGetOption","WlxGetOption callback function [Security]","_gina_wlxgetoption","security.wlxgetoption","winwlx/WlxGetOption"]
old-location: security\wlxgetoption.htm
tech.root: security
ms.assetid: 724477d4-ec56-44bd-801e-23c225bafd03
ms.date: 12/05/2018
ms.keywords: PWLX_GET_OPTION, PWLX_GET_OPTION callback, WlxGetOption, WlxGetOption callback function [Security], _gina_wlxgetoption, security.wlxgetoption, winwlx/WlxGetOption
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
 - PWLX_GET_OPTION
 - winwlx/PWLX_GET_OPTION
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
 - WlxGetOption
---

# PWLX_GET_OPTION callback function


## -description

<p class="CCE_Message">[The WlxGetOption function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to retrieve the current value of an option.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param Option [in]

Specifies one of the following options:

### -param Value [out]

Returns the current value of the option.

## -returns

The <b>WlxGetOption</b> function returns one of the following values.

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
The value of the option was returned in the <i>Value</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Winlogon did not return the value.

</td>
</tr>
</table>

## -remarks

In order to access this function, the GINA DLL must use the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a> structure and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_option">WlxSetOption</a>
