---
UID: NF:winwlx.WlxDisplayStatusMessage
title: WlxDisplayStatusMessage function (winwlx.h)
description: Winlogon calls this function when the GINA DLL should display a message.
helpviewer_keywords: ["WlxDisplayStatusMessage","WlxDisplayStatusMessage function [Security]","_gina_wlxdisplaystatusmessage","security.wlxdisplaystatusmessage","winwlx/WlxDisplayStatusMessage"]
old-location: security\wlxdisplaystatusmessage.htm
tech.root: security
ms.assetid: 07df61ff-f5fa-44ab-b3ca-ed7f4338e471
ms.date: 12/05/2018
ms.keywords: WlxDisplayStatusMessage, WlxDisplayStatusMessage function [Security], _gina_wlxdisplaystatusmessage, security.wlxdisplaystatusmessage, winwlx/WlxDisplayStatusMessage
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
 - WlxDisplayStatusMessage
 - winwlx/WlxDisplayStatusMessage
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
 - WlxDisplayStatusMessage
---

# WlxDisplayStatusMessage function


## -description

<p class="CCE_Message">[The WlxDisplayStatusMessage function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxDisplayStatusMessage</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function when the GINA DLL should display a message.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param hDesktop [in]

A handle to the desktop where the status message should be displayed.

### -param dwOptions [in]

Specifies display options for the status dialog box. The following options are valid: 




STATUSMSG_OPTION_NOANIMATION

STATUSMSG_OPTION_SETFOREGROUND

### -param pTitle [in]

Pointer to a null-terminated wide character string that specifies the title of the message to be displayed.

### -param pMessage [in]

Pointer to a null-terminated wide character string that specifies the message to be displayed.

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
Returns <b>TRUE</b> if the message was displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>FALSE</b> if the message was not displayed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>