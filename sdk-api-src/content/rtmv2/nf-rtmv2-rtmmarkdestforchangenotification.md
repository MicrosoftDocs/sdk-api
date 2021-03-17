---
UID: NF:rtmv2.RtmMarkDestForChangeNotification
title: RtmMarkDestForChangeNotification function (rtmv2.h)
description: The RtmMarkDestForChangeNotification function marks a destination for a client.
helpviewer_keywords: ["RtmMarkDestForChangeNotification","RtmMarkDestForChangeNotification function [RAS]","_rtmv2ref_rtmmarkdestforchangenotification","rras.rtmmarkdestforchangenotification","rtmv2/RtmMarkDestForChangeNotification"]
old-location: rras\rtmmarkdestforchangenotification.htm
tech.root: RRAS
ms.assetid: b7db8664-2775-4f96-8e5b-5062a8abcfe0
ms.date: 12/05/2018
ms.keywords: RtmMarkDestForChangeNotification, RtmMarkDestForChangeNotification function [RAS], _rtmv2ref_rtmmarkdestforchangenotification, rras.rtmmarkdestforchangenotification, rtmv2/RtmMarkDestForChangeNotification
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtmMarkDestForChangeNotification
 - rtmv2/RtmMarkDestForChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmMarkDestForChangeNotification
---

# RtmMarkDestForChangeNotification function


## -description

The 
<b>RtmMarkDestForChangeNotification</b> function marks a destination for a client. A marked destination indicates to the routing table manager that it should send the client change notification messages for the marked destination. The client receives change notification messages when a destination changes. The change notifications inform the client of changes to best-route information for the specified destination. This function should be used when 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a> is called to request changes for specific destinations (RTM_NOTIFY_ONLY_MARKED_DESTS).

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NotifyHandle [in]

Handle to a change notification obtained via a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

### -param DestHandle [in]

Handle to the destination that the client is marking for notification of changes.

### -param MarkDest [in]

Specifies whether to mark a destination and receive change notifications. Specify <b>TRUE</b> to mark a destination and start receive change notifications for the specified destination. Specify <b>FALSE</b> to stop receiving change notifications a previously marked destination.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangestatus">RtmGetChangeStatus</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmignorechangeddests">RtmIgnoreChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmismarkedforchangenotification">RtmIsMarkedForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>