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

# _DHCP_FILTER_ENUM_INFO structure


## -description


The <b>DHCP_FILTER_ENUM_INFO</b> structure contains information regarding the number of link-layer filter records.


## -struct-fields




### -field NumElements

Integer value that specifies the number of link-layer filter records contained in the array specified by pEnumRecords.


### -field pEnumRecords

Pointer to an array of <a href="https://msdn.microsoft.com/5f8531fe-cc30-4baf-904b-15627d1ff750">DHCP_FILTER_RECORD</a> structures that contain link-layer filter records.


### -field pEnumRecords.size_is

 


### -field pEnumRecords.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/5f8531fe-cc30-4baf-904b-15627d1ff750">DHCP_FILTER_RECORD</a>
 

 

