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

# IWMStreamConfig2::SetTransportType


## -description



The <b>SetTransportType</b> method sets the type of data communication protocol (reliable or unreliable) used for the stream.




## -parameters




### -param nTransportType [in]

One member of the <a href="https://msdn.microsoft.com/1d689487-f71b-4b27-928c-c55bd22579ed">WMT_TRANSPORT_TYPE</a> enumeration type specifying the transport type for the stream.


## -returns



The method always returns S_OK.




## -remarks



The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/dfe7b285-8d1d-4b71-a839-1c73d76e6444">IWMStreamConfig2::GetTransportType</a>
 

 

