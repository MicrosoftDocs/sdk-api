---
UID: NF:winwlx.WlxGetStatusMessage
title: WlxGetStatusMessage function (winwlx.h)
description: Winlogon calls this function to get the status message being displayed by the GINA DLL.
helpviewer_keywords: ["WlxGetStatusMessage","WlxGetStatusMessage function [Security]","_gina_wlxgetstatusmessage","security.wlxgetstatusmessage","winwlx/WlxGetStatusMessage"]
old-location: security\wlxgetstatusmessage.htm
tech.root: security
ms.assetid: 16208bbe-e697-4e75-8a28-a6d311ecb46c
ms.date: 12/05/2018
ms.keywords: WlxGetStatusMessage, WlxGetStatusMessage function [Security], _gina_wlxgetstatusmessage, security.wlxgetstatusmessage, winwlx/WlxGetStatusMessage
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
 - WlxGetStatusMessage
 - winwlx/WlxGetStatusMessage
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
 - WlxGetStatusMessage
---

# WlxGetStatusMessage function


## -description

<p class="CCE_Message">[The WlxGetStatusMessage function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxGetStatusMessage</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function to get the status message being displayed by the GINA DLL.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param pdwOptions [out]

Pointer to a <b>DWORD</b> that will hold the display options for the current status message.

### -param pMessage [out]

Returns the current status message text.

### -param dwBufferSize [in]

Size of the <i>pMessage</i> buffer.

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
Returns <b>TRUE</b> if the message was retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>FALSE</b> if the message was not retrieved.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxdisplaystatusmessage">WlxDisplayStatusMessage</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxremovestatusmessage">WlxRemoveStatusMessage</a>