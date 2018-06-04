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

# IVideoFrameStep::CanStep


## -description



The <code>CanStep</code> method determines the stepping capabilities of the specified filter.




## -parameters




### -param bMultiple

If <i>bMultiple</i> is zero and the method returns S_OK, the graph can step one frame at a time. If <i>bMultiple</i> if greater than zero and the method returns S_OK, the graph can step <i>bMultiple</i> frames at a time.


### -param pStepObject

Pointer to an interface on the filter that will control the stepping operation. Specify <b>NULL</b> to perform frame stepping using the renderer filter in the graph. If the graph includes a custom filter that implements the frame stepping, then <i>pStepObject</i> should specify that filter's <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface.


## -returns



Returns S_OK if the object can step or E_INVALIDARG if <i>pStepObject</i> is invalid.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7bf45473-144c-49f8-8178-aff5b60112b6">IVideoFrameStep Interface</a>
 

 

