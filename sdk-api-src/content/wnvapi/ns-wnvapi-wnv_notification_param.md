---
UID: NS:wnvapi._WNV_NOTIFICATION_PARAM
title: WNV_NOTIFICATION_PARAM (wnvapi.h)
description: Specifies the version, notification type, and the buffer location in a WnvRequestNotification function call.
helpviewer_keywords: ["*PWNV_NOTIFICATION_PARAM","PWNV_NOTIFICATION_PARAM","PWNV_NOTIFICATION_PARAM structure pointer [Windows Network Virtualization]","WNV_NOTIFICATION_PARAM","WNV_NOTIFICATION_PARAM structure [Windows Network Virtualization]","wnv.wnv_notification_param","wnvapi/PWNV_NOTIFICATION_PARAM","wnvapi/WNV_NOTIFICATION_PARAM"]
old-location: wnv\wnv_notification_param.htm
tech.root: wnv
ms.assetid: C8A27B21-462A-4D70-AA19-743023FD1810
ms.date: 12/05/2018
ms.keywords: '*PWNV_NOTIFICATION_PARAM, PWNV_NOTIFICATION_PARAM, PWNV_NOTIFICATION_PARAM structure pointer [Windows Network Virtualization], WNV_NOTIFICATION_PARAM, WNV_NOTIFICATION_PARAM structure [Windows Network Virtualization], wnv.wnv_notification_param, wnvapi/PWNV_NOTIFICATION_PARAM, wnvapi/WNV_NOTIFICATION_PARAM'
req.header: wnvapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WNV_NOTIFICATION_PARAM, *PWNV_NOTIFICATION_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_NOTIFICATION_PARAM
 - wnvapi/_WNV_NOTIFICATION_PARAM
 - PWNV_NOTIFICATION_PARAM
 - wnvapi/PWNV_NOTIFICATION_PARAM
 - WNV_NOTIFICATION_PARAM
 - wnvapi/WNV_NOTIFICATION_PARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_NOTIFICATION_PARAM
---

# WNV_NOTIFICATION_PARAM structure


## -description

Specifies the version, notification type, and the buffer location in a <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function call. The buffer specified in this structure is filled by the Windows Network Virtualization (WNV) driver when the notifications of the specific type are available.

## -struct-fields

### -field Header

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_object_header">WNV_OBJECT_HEADER</a></b>

The version and buffer size for this structure.

### -field NotificationType

Type: <b><a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_notification_type">WNV_NOTIFICATION_TYPE</a></b>

A value of the <a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_notification_type">WNV_NOTIFICATION_TYPE</a> enumeration that specifies the type of notifications requested, such as policy mismatches, Internet Control Message Protocol
(ICMP) redirect message arrivals, and object changes.

### -field PendingNotifications

Type: <b>ULONG</b>

An output value that provides the caller information about the number of pending events of the specified notification type. The pending events are queued within the WNV driver along with the events that have already been added to the <b>Buffer</b> field when the current <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function call is completed. This field allows the WNV driver to indicate the number of remaining events to the caller of <b>WnvRequestNotification</b>, so the caller can estimate the size of the buffer required. The caller should post another call with enough buffer size to <b>WnvRequestNotification</b> to consume these remaining events.

### -field Buffer

Type: <b>PUCHAR</b>

A pointer to a  buffer that is filled by the WNV driver with notification structures of the specified notification type when completing the call to <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a>. The eventual content in this field is explained by the following table.

<table>
<tr>
<th>Value of the <b>NotificationType</b> field</th>
<th>Content of the <b>Buffer</b> field</th>
</tr>
<tr>
<td><b>WnvPolicyMismatchType</b></td>
<td>
One or more <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_policy_mismatch_param">WNV_POLICY_MISMATCH_PARAM</a> structures

</td>
</tr>
<tr>
<td><b>WnvRedirectType</b></td>
<td>
One or more <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_redirect_param">WNV_REDIRECT_PARAM</a> structures

</td>
</tr>
<tr>
<td><b>WnvObjectChangeType</b></td>
<td>
One or more <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_object_change_param">WNV_OBJECT_CHANGE_PARAM</a> structures

</td>
</tr>
</table>