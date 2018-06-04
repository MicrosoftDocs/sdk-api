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

# IPersistMediaPropertyBag::InitNew


## -description



The <code>InitNew</code> method initializes the object to receive new properties.




## -parameters






## -returns



Returns S_OK.




## -remarks



Calling this method on the <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux</a> filter clears any properties that were previously set using the <a href="https://msdn.microsoft.com/02ee3911-0b85-404d-81c9-7d0e6b3ccd5d">Load</a> method.

Calling this method on the <a href="https://msdn.microsoft.com/df3c7d11-7ecc-499a-af36-b74437e21999">AVI Splitter</a> filter or the <a href="https://msdn.microsoft.com/53a9538d-7a79-40bb-9468-d710eb238925">WAVE Parser</a> filter has no effect.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/33e4b76b-841a-4dc5-b117-e08a6f4dcbe7">IPersistMediaPropertyBag Interface</a>
 

 

