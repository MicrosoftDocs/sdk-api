---
UID: NF:winwlx.WlxRemoveStatusMessage
title: WlxRemoveStatusMessage function (winwlx.h)
description: Winlogon calls this function to tell the GINA DLL to stop displaying the status message.
helpviewer_keywords: ["WlxRemoveStatusMessage","WlxRemoveStatusMessage function [Security]","_gina_wlxremovestatusmessage","security.wlxremovestatusmessage","winwlx/WlxRemoveStatusMessage"]
old-location: security\wlxremovestatusmessage.htm
tech.root: security
ms.assetid: b8e64f7b-04fc-4dbe-8670-314ff8838ba4
ms.date: 12/05/2018
ms.keywords: WlxRemoveStatusMessage, WlxRemoveStatusMessage function [Security], _gina_wlxremovestatusmessage, security.wlxremovestatusmessage, winwlx/WlxRemoveStatusMessage
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
 - WlxRemoveStatusMessage
 - winwlx/WlxRemoveStatusMessage
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
 - WlxRemoveStatusMessage
---

# WlxRemoveStatusMessage function


## -description

<p class="CCE_Message">[The WlxRemoveStatusMessage function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxRemoveStatusMessage</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function to tell the GINA DLL to stop displaying the status message.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

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
Return <b>TRUE</b> if the message was removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Return <b>FALSE</b> if the message was not removed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxdisplaystatusmessage">WlxDisplayStatusMessage</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxgetstatusmessage">WlxGetStatusMessage</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>