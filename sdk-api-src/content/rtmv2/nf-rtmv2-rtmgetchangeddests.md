---
UID: NF:rtmv2.RtmGetChangedDests
title: RtmGetChangedDests function (rtmv2.h)
description: The RtmGetChangedDests function returns a set of destinations with changed information.
helpviewer_keywords: ["RtmGetChangedDests","RtmGetChangedDests function [RAS]","_rtmv2ref_rtmgetchangeddests","rras.rtmgetchangeddests","rtmv2/RtmGetChangedDests"]
old-location: rras\rtmgetchangeddests.htm
tech.root: RRAS
ms.assetid: 2b22927d-a857-4bcb-9d89-6ca156b04ea9
ms.date: 12/05/2018
ms.keywords: RtmGetChangedDests, RtmGetChangedDests function [RAS], _rtmv2ref_rtmgetchangeddests, rras.rtmgetchangeddests, rtmv2/RtmGetChangedDests
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
 - RtmGetChangedDests
 - rtmv2/RtmGetChangedDests
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
 - RtmGetChangedDests
---

# RtmGetChangedDests function


## -description

The 
<b>RtmGetChangedDests</b> function returns a set of destinations with changed information.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NotifyHandle [in]

Handle to a change notification obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

### -param NumDests [in, out]

On input, <i>NumDests</i> is a pointer to a <b>UINT</b> value that specifies the maximum number of destinations that can be received by <i>ChangedDests</i>. 




On output, <i>NumDests</i> receives the actual number of destinations received by <i>ChangedDests</i>.

### -param ChangedDests [out]

On input, <i>ChangedDests</i> is a pointer to an array of 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structures. 




On output, <i>ChangedDests</i> is filled with the changed destination information.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains incorrect information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more changed destinations to retrieve.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

A client is notified of changes by an 
<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a>. The 
<b>RTM_EVENT_CALLBACK</b> is only used to notify the client, not deliver the changes. After a change notification is received, the client must call 
<b>RtmGetChangedDests</b> repeatedly to retrieve all the changes.

If two or more changes to the same destination have occurred since the notification, only the latest change is returned.

When a client no longer needs the handles in <i>ChangedDests</i>, the client must use 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a> to release the handles.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/use-the-event-notification-callback">Use the Event Notification Callback</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a>



<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangestatus">RtmGetChangeStatus</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmignorechangeddests">RtmIgnoreChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmismarkedforchangenotification">RtmIsMarkedForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>