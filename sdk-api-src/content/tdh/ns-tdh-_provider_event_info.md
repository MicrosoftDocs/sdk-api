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

# _PROVIDER_EVENT_INFO structure


## -description


The <b>PROVIDER_EVENT_INFO</b> structure defines an array of events in a provider manifest.


## -struct-fields




### -field NumberOfEvents

The number of elements in the <b>EventDescriptorsArray</b> array.


### -field Reserved

Reserved.


### -field EventDescriptorsArray

An array of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structures that contain information about each event.


## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/93A03E1D-4047-49F1-987B-FB7BE03E0483">TdhEnumerateManifestProviderEvents</a>



<a href="https://msdn.microsoft.com/71702F1F-1708-4CA2-9BFB-3D7332AB6129">TdhGetManifestEventInformation</a>
 

 

