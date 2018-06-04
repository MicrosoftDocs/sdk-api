---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WNV_NOTIFICATION_PARAM structure


## -description


Specifies the version, notification type, and the buffer location in a <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a> function call. The buffer specified in this structure is filled by the Windows Network Virtualization (WNV) driver when the notifications of the specific type are available.


## -struct-fields




### -field Header

Type: <b><a href="https://msdn.microsoft.com/3D139C56-0224-4120-B308-A33F257DD9DC">WNV_OBJECT_HEADER</a></b>

The version and buffer size for this structure.


### -field NotificationType

Type: <b><a href="https://msdn.microsoft.com/70BE564E-A054-4991-ADCD-79E4D219307B">WNV_NOTIFICATION_TYPE</a></b>

A value of the <a href="https://msdn.microsoft.com/70BE564E-A054-4991-ADCD-79E4D219307B">WNV_NOTIFICATION_TYPE</a> enumeration that specifies the type of notifications requested, such as policy mismatches, Internet Control Message Protocol
(ICMP) redirect message arrivals, and object changes.


### -field PendingNotifications

Type: <b>ULONG</b>

An output value that provides the caller information about the number of pending events of the specified notification type. The pending events are queued within the WNV driver along with the events that have already been added to the <b>Buffer</b> field when the current <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a> function call is completed. This field allows the WNV driver to indicate the number of remaining events to the caller of <b>WnvRequestNotification</b>, so the caller can estimate the size of the buffer required. The caller should post another call with enough buffer size to <b>WnvRequestNotification</b> to consume these remaining events.


### -field Buffer

Type: <b>PUCHAR</b>

A pointer to a  buffer that is filled by the WNV driver with notification structures of the specified notification type when completing the call to <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a>. The eventual content in this field is explained by the following table.

<table>
<tr>
<th>Value of the <b>NotificationType</b> field</th>
<th>Content of the <b>Buffer</b> field</th>
</tr>
<tr>
<td><b>WnvPolicyMismatchType</b></td>
<td>
One or more <a href="https://msdn.microsoft.com/2781B0D6-950E-49AD-9B30-31DE4A27ED4A">WNV_POLICY_MISMATCH_PARAM</a> structures

</td>
</tr>
<tr>
<td><b>WnvRedirectType</b></td>
<td>
One or more <a href="https://msdn.microsoft.com/53305594-4539-490E-B034-99355265F175">WNV_REDIRECT_PARAM</a> structures

</td>
</tr>
<tr>
<td><b>WnvObjectChangeType</b></td>
<td>
One or more <a href="https://msdn.microsoft.com/12FF591A-B696-49DF-9E75-B966569A2AAE">WNV_OBJECT_CHANGE_PARAM</a> structures

</td>
</tr>
</table>
 

