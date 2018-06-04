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

# IWMReaderAccelerator::Notify


## -description



The <b>Notify</b> method is called by the source filter to pass in the negotiated media type.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> that specifies the stream associated with the notification.


### -param pSubtype [in]

Pointer to a media type that describes the current connection parameters for the stream.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code .




## -remarks



This method enables the reader to update its internal variables and commit to the DirectX VA connection. This is the last place the decoder or reader can fail.




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/cf783b70-4d19-4006-ad0e-e1f883f00b0b">IWMReaderAccelerator Interface</a>
 

 

