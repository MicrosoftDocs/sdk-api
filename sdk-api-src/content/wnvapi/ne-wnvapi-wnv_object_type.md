---
UID: NE:wnvapi._WNV_OBJECT_TYPE
title: WNV_OBJECT_TYPE (wnvapi.h)
description: Specifies the object type of a given Windows Network Virtualization (WNV) notification when the WNV notification type is WnvObjectChangeType.
helpviewer_keywords: ["*PWNV_OBJECT_TYPE","PWNV_OBJECT_TYPE","PWNV_OBJECT_TYPE enumeration pointer [Windows Network Virtualization]","WNV_OBJECT_TYPE","WNV_OBJECT_TYPE enumeration [Windows Network Virtualization]","WnvObjectTypeMax","WnvProviderAddressType","wnv.wnv_object_type","wnvapi/PWNV_OBJECT_TYPE","wnvapi/WNV_OBJECT_TYPE","wnvapi/WnvObjectTypeMax","wnvapi/WnvProviderAddressType"]
old-location: wnv\wnv_object_type.htm
tech.root: wnv
ms.assetid: 817C86BB-1267-4174-93C2-515288A33055
ms.date: 12/05/2018
ms.keywords: '*PWNV_OBJECT_TYPE, PWNV_OBJECT_TYPE, PWNV_OBJECT_TYPE enumeration pointer [Windows Network Virtualization], WNV_OBJECT_TYPE, WNV_OBJECT_TYPE enumeration [Windows Network Virtualization], WnvObjectTypeMax, WnvProviderAddressType, wnv.wnv_object_type, wnvapi/PWNV_OBJECT_TYPE, wnvapi/WNV_OBJECT_TYPE, wnvapi/WnvObjectTypeMax, wnvapi/WnvProviderAddressType'
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
req.typenames: WNV_OBJECT_TYPE, *PWNV_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_OBJECT_TYPE
 - wnvapi/_WNV_OBJECT_TYPE
 - PWNV_OBJECT_TYPE
 - wnvapi/PWNV_OBJECT_TYPE
 - WNV_OBJECT_TYPE
 - wnvapi/WNV_OBJECT_TYPE
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
 - WNV_OBJECT_TYPE
---

# WNV_OBJECT_TYPE enumeration


## -description

Specifies the object type of a given Windows Network Virtualization (WNV) notification when the WNV notification type is <b>WnvObjectChangeType</b>.

## -enum-fields

### -field WnvProviderAddressType

The notification is about a change in a property of a provider address object.

### -field WnvCustomerAddressType

### -field WnvObjectTypeMax

The maximum possible value for this enumeration type. This is not a legal value.

## -see-also

<a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_notification_type">WNV_NOTIFICATION_TYPE</a>



<a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_object_change_param">WNV_OBJECT_CHANGE_PARAM</a>