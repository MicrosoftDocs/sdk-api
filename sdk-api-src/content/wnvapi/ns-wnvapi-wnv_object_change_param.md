---
UID: NS:wnvapi._WNV_OBJECT_CHANGE_PARAM
title: WNV_OBJECT_CHANGE_PARAM (wnvapi.h)
description: Specifies the parameters of an event that causes the Windows Network Virtualization (WNV) driver to generate a WnvObjectChangeType type of notification.
helpviewer_keywords: ["*PWNV_OBJECT_CHANGE_PARAM","PWNV_OBJECT_CHANGE_PARAM","PWNV_OBJECT_CHANGE_PARAM structure pointer [Windows Network Virtualization]","WNV_OBJECT_CHANGE_PARAM","WNV_OBJECT_CHANGE_PARAM structure [Windows Network Virtualization]","wnv.wnv_object_change_param","wnvapi/PWNV_OBJECT_CHANGE_PARAM","wnvapi/WNV_OBJECT_CHANGE_PARAM"]
old-location: wnv\wnv_object_change_param.htm
tech.root: wnv
ms.assetid: 12FF591A-B696-49DF-9E75-B966569A2AAE
ms.date: 12/05/2018
ms.keywords: '*PWNV_OBJECT_CHANGE_PARAM, PWNV_OBJECT_CHANGE_PARAM, PWNV_OBJECT_CHANGE_PARAM structure pointer [Windows Network Virtualization], WNV_OBJECT_CHANGE_PARAM, WNV_OBJECT_CHANGE_PARAM structure [Windows Network Virtualization], wnv.wnv_object_change_param, wnvapi/PWNV_OBJECT_CHANGE_PARAM, wnvapi/WNV_OBJECT_CHANGE_PARAM'
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
req.typenames: WNV_OBJECT_CHANGE_PARAM, *PWNV_OBJECT_CHANGE_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_OBJECT_CHANGE_PARAM
 - wnvapi/_WNV_OBJECT_CHANGE_PARAM
 - PWNV_OBJECT_CHANGE_PARAM
 - wnvapi/PWNV_OBJECT_CHANGE_PARAM
 - WNV_OBJECT_CHANGE_PARAM
 - wnvapi/WNV_OBJECT_CHANGE_PARAM
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
 - WNV_OBJECT_CHANGE_PARAM
---

# WNV_OBJECT_CHANGE_PARAM structure


## -description

Specifies the parameters of an event  that causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvObjectChangeType</b> type of notification. If there is a pending call to the <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function of this type, the WNV driver fills the buffer that is passed in the <i>NotificationParam</i> argument's <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure with one or more instances of this structure and completes the <b>WnvRequestNotification</b> function call.

## -struct-fields

### -field ObjectType

Type: <b><a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_object_type">WNV_OBJECT_TYPE</a></b>

The object type that causes the change notification.

### -field ObjectParam

The parameters for the corresponding object type. If the object type is <b>WnvProviderAddressType</b>, this field points to the <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_provider_address_change_param">WNV_PROVIDER_ADDRESS_CHANGE_PARAM</a> structure that describes the provider address object that generated an object change event.

### -field ObjectParam.ProviderAddressChange

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_provider_address_change_param">WNV_PROVIDER_ADDRESS_CHANGE_PARAM</a></b>

The provider address change parameters for this object change event.

### -field ObjectParam.CustomerAddressChange

## -remarks

There is currently only one type of object defined and tracked in this structure: <b>WnvProviderAddressType</b>.

## -see-also

<a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_notification_type">WNV_NOTIFICATION_TYPE</a>