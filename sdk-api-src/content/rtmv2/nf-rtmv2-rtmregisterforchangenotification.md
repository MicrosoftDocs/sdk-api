---
UID: NF:rtmv2.RtmRegisterForChangeNotification
title: RtmRegisterForChangeNotification function (rtmv2.h)
description: The RtmRegisterForChangeNotification function informs the routing table manager that the client should receive change notifications for the specified types of changes.
helpviewer_keywords: ["RTM_CHANGE_TYPE_ALL","RTM_CHANGE_TYPE_BEST","RTM_CHANGE_TYPE_FORWARDING","RTM_NOTIFY_ONLY_MARKED_DESTS","RtmRegisterForChangeNotification","RtmRegisterForChangeNotification function [RAS]","_rtmv2ref_rtmregisterforchangenotification","rras.rtmregisterforchangenotification","rtmv2/RtmRegisterForChangeNotification"]
old-location: rras\rtmregisterforchangenotification.htm
tech.root: RRAS
ms.assetid: b6e04984-ac92-44a2-a18c-018c6b1b49a9
ms.date: 12/05/2018
ms.keywords: RTM_CHANGE_TYPE_ALL, RTM_CHANGE_TYPE_BEST, RTM_CHANGE_TYPE_FORWARDING, RTM_NOTIFY_ONLY_MARKED_DESTS, RtmRegisterForChangeNotification, RtmRegisterForChangeNotification function [RAS], _rtmv2ref_rtmregisterforchangenotification, rras.rtmregisterforchangenotification, rtmv2/RtmRegisterForChangeNotification
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
 - RtmRegisterForChangeNotification
 - rtmv2/RtmRegisterForChangeNotification
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
 - RtmRegisterForChangeNotification
---

# RtmRegisterForChangeNotification function


## -description

The 
<b>RtmRegisterForChangeNotification</b> function informs the routing table manager that the client should receive change notifications for the specified types of changes. The routing table manager returns a change notification handle, which the client must use when requesting change information after receiving a change notification message.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param TargetViews [in]

Specifies the views in which to register for change notification.

### -param NotifyFlags [in]

Specifies the flags that indicate the type of changes for which the client requests notification. The following flags are used. (The flags are to be joined using a logical OR.) 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_CHANGE_TYPE_ALL"></a><a id="rtm_change_type_all"></a><dl>
<dt><b>RTM_CHANGE_TYPE_ALL</b></dt>
</dl>
</td>
<td width="60%">
Notify the client of any change to a destination.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_CHANGE_TYPE_BEST"></a><a id="rtm_change_type_best"></a><dl>
<dt><b>RTM_CHANGE_TYPE_BEST</b></dt>
</dl>
</td>
<td width="60%">
Notify the client of changes to the current best route, or when the best route changes.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_CHANGE_TYPE_FORWARDING"></a><a id="rtm_change_type_forwarding"></a><dl>
<dt><b>RTM_CHANGE_TYPE_FORWARDING</b></dt>
</dl>
</td>
<td width="60%">
Notify the client of any best route changes that affect forwarding, such as next hop changes.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_NOTIFY_ONLY_MARKED_DESTS"></a><a id="rtm_notify_only_marked_dests"></a><dl>
<dt><b>RTM_NOTIFY_ONLY_MARKED_DESTS</b></dt>
</dl>
</td>
<td width="60%">
Notify the client of changes to destinations that the client has marked. If this flag is not specified, change notification messages for all destinations are sent.

</td>
</tr>
</table>

### -param NotifyContext [in]

Specifies the notification context that the 
<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a> uses to indicate new changes. The notification context is the <i>Context2</i> parameter of the 
<b>RTM_EVENT_CALLBACK</b> callback.

### -param NotifyHandle [out]

Receives a handle to a change notification. The handle must be used when calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>.

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
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There are not enough available system resources to complete this operation. The routing table manager has exceeded the maximum number of change notifications that can be cached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
One or more of the specified views is not supported.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

A client calls 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a> when it is registering for changes to a specific destination.

The routing table manager uses the 
<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a> callback, specified when the client called 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>, to notify the client when changes have occurred; the client must call 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a> to receive the actual change information.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/register-for-change-notification">Register For Change Notification</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmderegisterfromchangenotification">RtmDeregisterFromChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>