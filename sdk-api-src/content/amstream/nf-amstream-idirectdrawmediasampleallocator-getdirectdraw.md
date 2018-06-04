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

# IDirectDrawMediaSampleAllocator::GetDirectDraw


## -description



The <code>GetDirectDraw</code> method retrieves a pointer to the DirectDraw instance used to allocate surfaces.




## -parameters




### -param ppDirectDraw [out]

Address of a pointer that receives the DirectDraw object's <b>IDirectDraw</b> interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The caller should release the returned <b>IDirectDraw</b> pointer, except when calling the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter's implementation of this interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/35fd81ce-058a-4caf-b1de-f669be586f33">IDirectDrawMediaSampleAllocator Interface</a>
 

 

