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

# CodecAPIEventData structure


## -description



The <b>CodecAPIEventData</b> structure contains event data for the <a href="https://msdn.microsoft.com/88924ba9-707b-41a7-9bca-c630b4a9c4c8">EC_CODECAPI_EVENT</a> event. This event is sent by codecs that support the <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a> interface.




## -struct-fields




### -field guid


            A GUID that identifies the codec event.
          


### -field dataLength


            The length of the additional data that follows this structure, in bytes.
          The value can be zero.


### -field reserved


            Reserved; do not use.
          


## -remarks



This structure may be followed by addition data, depending on the codec event. For more information, see <a href="https://msdn.microsoft.com/87423ddb-7011-40ab-a449-eb43688efb26">ICodecAPI::RegisterForEvent</a>
    .




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/87423ddb-7011-40ab-a449-eb43688efb26">ICodecAPI::RegisterForEvent</a>
 

 

