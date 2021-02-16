---
UID: NC:winwlx.PWLX_SET_TIMEOUT
title: PWLX_SET_TIMEOUT (winwlx.h)
description: Called by GINA to change the time-out associated with a dialog box. The default time-out is two minutes.
helpviewer_keywords: ["PWLX_SET_TIMEOUT","PWLX_SET_TIMEOUT callback","WlxSetTimeout","WlxSetTimeout callback function [Security]","_gina_wlxsettimeout","security.wlxsettimeout","winwlx/WlxSetTimeout"]
old-location: security\wlxsettimeout.htm
tech.root: security
ms.assetid: e5f1a184-195a-4a0e-849a-ed629a6c9049
ms.date: 12/05/2018
ms.keywords: PWLX_SET_TIMEOUT, PWLX_SET_TIMEOUT callback, WlxSetTimeout, WlxSetTimeout callback function [Security], _gina_wlxsettimeout, security.wlxsettimeout, winwlx/WlxSetTimeout
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
 - PWLX_SET_TIMEOUT
 - winwlx/PWLX_SET_TIMEOUT
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
 - WlxSetTimeout
---

# PWLX_SET_TIMEOUT callback function


## -description

<p class="CCE_Message">[The WlxSetTimeout function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to change the time-out associated with a dialog box. The default time-out is two minutes.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param Timeout [in]

Requested time-out, in seconds.

## -returns

The <b>WlxSetTimeout</b> function returns one of the following values.

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
The new time-out was accepted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The new time-out was not accepted.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>