---
UID: NS:wnvapi._WNV_OBJECT_CHANGE_PARAM
title: WNV_OBJECT_CHANGE_PARAM (wnvapi.h)
author: windows-sdk-content
description: Specifies the parameters of an event that causes the Windows Network Virtualization (WNV) driver to generate a WnvObjectChangeType type of notification.
old-location: wnv\wnv_object_change_param.htm
tech.root: wnv
ms.assetid: 12FF591A-B696-49DF-9E75-B966569A2AAE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWNV_OBJECT_CHANGE_PARAM, PWNV_OBJECT_CHANGE_PARAM, PWNV_OBJECT_CHANGE_PARAM structure pointer [Windows Network Virtualization], WNV_OBJECT_CHANGE_PARAM, WNV_OBJECT_CHANGE_PARAM structure [Windows Network Virtualization], wnv.wnv_object_change_param, wnvapi/PWNV_OBJECT_CHANGE_PARAM, wnvapi/WNV_OBJECT_CHANGE_PARAM"
ms.topic: struct
f1_keywords: ["wnvapi/WNV_OBJECT_CHANGE_PARAM"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_OBJECT_CHANGE_PARAM
product: Windows
targetos: Windows
req.typenames: WNV_OBJECT_CHANGE_PARAM, *PWNV_OBJECT_CHANGE_PARAM
req.redist: 
ms.custom: 19H1
---

# WNV_OBJECT_CHANGE_PARAM structure


## -description


Specifies the parameters of an event  that causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvObjectChangeType</b> type of notification. If there is a pending call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function of this type, the WNV driver fills the buffer that is passed in the <i>NotificationParam</i> argument's <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wnvapi/ns-wnvapi-_wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure with one or more instances of this structure and completes the <b>WnvRequestNotification</b> function call.


## -struct-fields




### -field ObjectType

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wnvapi/ne-wnvapi-_wnv_object_type">WNV_OBJECT_TYPE</a></b>

The object type that causes the change notification.


### -field ObjectParam

The parameters for the corresponding object type. If the object type is <b>WnvProviderAddressType</b>, this field points to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wnvapi/ns-wnvapi-_wnv_provider_address_change_param">WNV_PROVIDER_ADDRESS_CHANGE_PARAM</a> structure that describes the provider address object that generated an object change event.


### -field ObjectParam.ProviderAddressChange

<b>Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wnvapi/ns-wnvapi-_wnv_provider_address_change_param">WNV_PROVIDER_ADDRESS_CHANGE_PARAM</a></b>
</b>
The provider address change parameters for this object change event.


### -field ObjectParam.CustomerAddressChange

 




## -remarks



There is currently only one type of object defined and tracked in this structure: <b>WnvProviderAddressType</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wnvapi/ne-wnvapi-_wnv_notification_type">WNV_NOTIFICATION_TYPE</a>
 

 

