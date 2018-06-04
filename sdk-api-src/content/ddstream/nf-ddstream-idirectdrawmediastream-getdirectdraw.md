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

# IDirectDrawMediaStream::GetDirectDraw


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves a pointer to the DirectDraw object used by the current media stream.




## -parameters




### -param ppDirectDraw [out]

Address of a pointer to an <b>IDirectDraw</b> interface that will contain the current media stream's associated DirectDraw object.


## -returns



Returns S_OK if successful or E_POINTER if the parameter is invalid.




## -remarks



If you haven't initialized the stream yet, the retrieved pointer will be <b>NULL</b> and the method will return S_OK. If you have initialized the stream, this method increments the retrieved pointer's reference count.




## -see-also




<a href="https://msdn.microsoft.com/858af0c3-9e22-45d8-ab08-307eb39a8977">IDirectDrawMediaStream Interface</a>
 

 

