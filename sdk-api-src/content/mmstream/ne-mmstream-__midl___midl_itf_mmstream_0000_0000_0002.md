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

# __MIDL___MIDL_itf_mmstream_0000_0000_0002 enumeration


## -description



<div class="alert"><b>Note</b>  This API is deprecated. New applications should not use it.</div>
<div> </div>
Describes the state of the stream.




## -enum-fields




### -field STREAMSTATE_STOP

Stop state.


### -field STREAMSTATE_RUN

Run state.


## -remarks



Change the state by calling the <a href="https://msdn.microsoft.com/69c3612f-e91a-4ab3-8f6d-2966e64a9220">IMultiMediaStream::SetState</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0b2866cc-ff07-4cd9-b7df-6a05436251d3">Multimedia Streaming Enumeration Types</a>
 

 

