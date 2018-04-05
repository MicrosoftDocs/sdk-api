---
UID: NE:wnvapi._WNV_OBJECT_TYPE
title: "_WNV_OBJECT_TYPE"
author: windows-driver-content
description: Specifies the object type of a given Windows Network Virtualization (WNV) notification when the WNV notification type is WnvObjectChangeType.
old-location: wnv\wnv_object_type.htm
old-project: wnv
ms.assetid: 817C86BB-1267-4174-93C2-515288A33055
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PWNV_OBJECT_TYPE, PWNV_OBJECT_TYPE, PWNV_OBJECT_TYPE enumeration pointer [Windows Network Virtualization], WNV_OBJECT_TYPE, WNV_OBJECT_TYPE enumeration [Windows Network Virtualization], WnvObjectTypeMax, WnvProviderAddressType, _WNV_OBJECT_TYPE, wnv.wnv_object_type, wnvapi/PWNV_OBJECT_TYPE, wnvapi/WNV_OBJECT_TYPE, wnvapi/WnvObjectTypeMax, wnvapi/WnvProviderAddressType"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WNV_OBJECT_TYPE, *PWNV_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wnvapi.h
api_name:
-	WNV_OBJECT_TYPE
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WNV_OBJECT_TYPE enumeration


## -description


Specifies the object type of a given Windows Network Virtualization (WNV) notification when the WNV notification type is <b>WnvObjectChangeType</b>.


## -enum-fields




### -field WnvProviderAddressType

The notification is about a change in a property of a provider address object.


### -field WnvCustomerAddressType


### -field WnvObjectTypeMax

The maximum possible value for this enumeration type. This is not a legal value.


## -see-also




<a href="https://msdn.microsoft.com/70BE564E-A054-4991-ADCD-79E4D219307B">WNV_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/12FF591A-B696-49DF-9E75-B966569A2AAE">WNV_OBJECT_CHANGE_PARAM</a>
 

 

