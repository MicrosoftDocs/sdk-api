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

# _PROVIDER_ENUMERATION_INFO structure


## -description



		Defines the array of providers that have registered a MOF or manifest on the computer.


## -struct-fields




### -field NumberOfProviders

Number of elements in the <b>TraceProviderInfoArray</b> array.


### -field Reserved

 


### -field TraceProviderInfoArray

Array of <a href="https://msdn.microsoft.com/0dbfde78-b1d4-4cc6-99aa-81de3f647cdb">TRACE_PROVIDER_INFO</a> structures that contain information about each provider such as its name and unique identifier.


#### - Padding

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/ef326ef8-227d-46b5-88b9-b519748fb778">TdhEnumerateProviders</a>
 

 

