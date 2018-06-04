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

# IDirectManipulationViewportEventHandler::OnContentUpdated


## -description


Called when content inside a viewport is updated.



## -parameters




### -param viewport [in]

The viewport that is updated.


### -param content [in]

The content in the viewport that has changed.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method is called once for each  content change in the viewport. This can result in multiple <b>OnContentUpdated</b> calls. For instance, when the position of the content is changed, you can use <a href="https://msdn.microsoft.com/9db4f521-227c-4e2f-8c7d-44ae4a25651e">IDirectManipualtionContent::GetContentTransform</a> to retrieve the new value.

If you have actions that need to be executed once for a viewport update, implement <a href="https://msdn.microsoft.com/dfb70d6f-ce3c-4d39-b7b5-21812ff7e56b">OnViewportUpdated</a>.




## -see-also




<a href="https://msdn.microsoft.com/3594011a-da4a-4550-9b3b-076218d09f39">IDirectManipulationViewportEventHandler</a>
 

 

