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

# __MIDL___MIDL_itf_pla_0001_0043_0008 enumeration


## -description


Defines the type of the value.


## -enum-fields




### -field plaIndex

Only one item in the collection can be enabled. The enabled item is the value of the <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> property. If more than one item is enabled, the first enabled item is used as the value.


### -field plaFlag

One or more items in the collection can be enabled. An item in the collection represents a single bit flag. The enabled items in the collection are combined  with the <b>OR</b> operator to become the value of <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a>.


### -field plaFlagArray

The collection contains a list of Event Tracing for Windows extended flags (see the <a href="https://msdn.microsoft.com/1dc21423-fa55-4312-b86a-63d4f59e4cf1">ITraceDataProvider::Properties</a> property).


### -field plaValidation

The collection contains a list of HRESULT values returned by the validation process.


## -see-also




<a href="https://msdn.microsoft.com/42cea1e6-c945-4bae-ac65-a052b4069e5f">IValueMap::ValueMapType</a>



<a href="https://msdn.microsoft.com/006d134d-d14b-4964-b46c-7dd2353d2493">IValueMapItem::ValueMapType</a>
 

 

