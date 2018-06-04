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

# IAMWMBufferPassCallback::Notify


## -description



The <code>Notify</code> method is called by the pin for each buffer that is delivered during streaming.




## -parameters




### -param pNSSBuffer3 [in]

Pointer to the <a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3</a> interface of the media sample.


### -param pPin [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of the pin that has delivered or received the sample.


### -param prtStart [in]

Start time of the sample, in 100-nanosecond units.


### -param prtEnd [in]

End time of the sample, in 100-nanosecond units.


## -returns



No particular return value is specified. The calling pin ignores the <b>HRESULT</b>.




## -remarks



This method enables an application to examine and act on information in the media buffer before the buffer contents are processed. The application is responsible for knowing the media type on the pin. This information can be obtained by first getting the stream information from the profile and then calling <a href="https://msdn.microsoft.com/374331ec-6665-4ed9-b4ee-6d33b1e2ef2c">IConfigAsfWriter2::StreamNumFromPin</a> method to determine which pin is associated with each stream. Alternatively, you can call <a href="https://msdn.microsoft.com/f372bfa7-b0ba-43f9-ba86-cbca5d1de515">IPin::ConnectionMediaType</a> on the pin.




## -see-also




<a href="https://msdn.microsoft.com/c3a8e01e-a626-4e47-ad98-e22d1fe88906">IAMWMBufferPassCallback Interface</a>



<a href="https://msdn.microsoft.com/2fae0504-d1da-413a-80dd-de7818f506ef">Using Windows Media in DirectShow</a>
 

 

