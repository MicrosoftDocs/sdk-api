---
UID: NE:wnvapi._WNV_NOTIFICATION_TYPE
title: "_WNV_NOTIFICATION_TYPE"
author: windows-sdk-content
description: Specifies the type of a given Windows Network Virtualization (WNV) notification.
old-location: wnv\wnv_notification_type.htm
old-project: wnv
ms.assetid: 70BE564E-A054-4991-ADCD-79E4D219307B
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PWNV_NOTIFICATION_TYPE, PWNV_NOTIFICATION_TYPE, PWNV_NOTIFICATION_TYPE enumeration pointer [Windows Network Virtualization], WNV_NOTIFICATION_TYPE, WNV_NOTIFICATION_TYPE enumeration [Windows Network Virtualization], WnvNotificationTypeMax, WnvObjectChangeType, WnvPolicyMismatchType, WnvRedirectType, _WNV_NOTIFICATION_TYPE, wnv.wnv_notification_type, wnvapi/PWNV_NOTIFICATION_TYPE, wnvapi/WNV_NOTIFICATION_TYPE, wnvapi/WnvNotificationTypeMax, wnvapi/WnvObjectChangeType, wnvapi/WnvPolicyMismatchType, wnvapi/WnvRedirectType"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: WNV_NOTIFICATION_TYPE, *PWNV_NOTIFICATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wnvapi.h
api_name:
-	WNV_NOTIFICATION_TYPE
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WNV_NOTIFICATION_TYPE enumeration


## -description


Specifies the type of a given Windows Network Virtualization (WNV) notification.


## -enum-fields




### -field WnvPolicyMismatchType

A policy mismatch notification.


### -field WnvRedirectType

A notification that an Internet Control Message Protocol
(ICMP) redirect message has been received.


### -field WnvObjectChangeType

A notification that a network object has changed.


### -field WnvNotificationTypeMax

The maximum possible value for this enumeration type. This is not a legal value.


## -see-also




<a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">WNV_NOTIFICATION_PARAM</a>
 

 

