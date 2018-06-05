---
UID: NS:wnvapi._WNV_NOTIFICATION_PARAM
title: "_WNV_NOTIFICATION_PARAM"
author: windows-sdk-content
description: Specifies the version, notification type, and the buffer location in a WnvRequestNotification function call.
old-location: wnv\wnv_notification_param.htm
old-project: wnv
ms.assetid: C8A27B21-462A-4D70-AA19-743023FD1810
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PWNV_NOTIFICATION_PARAM, PWNV_NOTIFICATION_PARAM, PWNV_NOTIFICATION_PARAM structure pointer [Windows Network Virtualization], WNV_NOTIFICATION_PARAM, WNV_NOTIFICATION_PARAM structure [Windows Network Virtualization], _WNV_NOTIFICATION_PARAM, wnv.wnv_notification_param, wnvapi/PWNV_NOTIFICATION_PARAM, wnvapi/WNV_NOTIFICATION_PARAM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WNV_NOTIFICATION_PARAM, *PWNV_NOTIFICATION_PARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wnvapi.h
api_name:
-	WNV_NOTIFICATION_PARAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

