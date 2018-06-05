---
UID: NS:wnvapi._WNV_OBJECT_CHANGE_PARAM
title: "_WNV_OBJECT_CHANGE_PARAM"
author: windows-sdk-content
description: Specifies the parameters of an event that causes the Windows Network Virtualization (WNV) driver to generate a WnvObjectChangeType type of notification.
old-location: wnv\wnv_object_change_param.htm
old-project: wnv
ms.assetid: 12FF591A-B696-49DF-9E75-B966569A2AAE
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PWNV_OBJECT_CHANGE_PARAM, PWNV_OBJECT_CHANGE_PARAM, PWNV_OBJECT_CHANGE_PARAM structure pointer [Windows Network Virtualization], WNV_OBJECT_CHANGE_PARAM, WNV_OBJECT_CHANGE_PARAM structure [Windows Network Virtualization], _WNV_OBJECT_CHANGE_PARAM, wnv.wnv_object_change_param, wnvapi/PWNV_OBJECT_CHANGE_PARAM, wnvapi/WNV_OBJECT_CHANGE_PARAM"
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
req.typenames: WNV_OBJECT_CHANGE_PARAM, *PWNV_OBJECT_CHANGE_PARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wnvapi.h
api_name:
-	WNV_OBJECT_CHANGE_PARAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WNV_OBJECT_CHANGE_PARAM structure


## -description


Specifies the parameters of an event  that causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvObjectChangeType</b> type of notification. If there is a pending call to the <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a> function of this type, the WNV driver fills the buffer that is passed in the <i>NotificationParam</i> argument's <a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">WNV_NOTIFICATION_PARAM</a> structure with one or more instances of this structure and completes the <b>WnvRequestNotification</b> function call.


## -struct-fields




### -field ObjectType

Type: <b><a href="https://msdn.microsoft.com/817C86BB-1267-4174-93C2-515288A33055">WNV_OBJECT_TYPE</a></b>

The object type that causes the change notification.


### -field ObjectParam

The parameters for the corresponding object type. If the object type is <b>WnvProviderAddressType</b>, this field points to the <a href="https://msdn.microsoft.com/9FC20DFE-663C-47ED-8183-76C10D4E7615">WNV_PROVIDER_ADDRESS_CHANGE_PARAM</a> structure that describes the provider address object that generated an object change event.


### -field ObjectParam.ProviderAddressChange

<b>Type: <b><a href="https://msdn.microsoft.com/9FC20DFE-663C-47ED-8183-76C10D4E7615">WNV_PROVIDER_ADDRESS_CHANGE_PARAM</a></b>
</b>
The provider address change parameters for this object change event.


### -field ObjectParam.CustomerAddressChange

 




## -remarks



There is currently only one type of object defined and tracked in this structure: <b>WnvProviderAddressType</b>.




## -see-also




<a href="https://msdn.microsoft.com/70BE564E-A054-4991-ADCD-79E4D219307B">WNV_NOTIFICATION_TYPE</a>
 

 

