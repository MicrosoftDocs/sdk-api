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

# IDirectManipulationViewportEventHandler::OnViewportUpdated


## -description


Called after all content in the viewport has been updated.


## -parameters




### -param viewport [in]

The viewport that has been updated.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If you have actions that need to be executed once for a viewport update, implement <b>OnViewportUpdated</b>. <a href="https://msdn.microsoft.com/1b9a0f54-ccc7-4927-a34e-724652f6c2f0">OnContentUpdated</a> is called once for each  content change in the viewport. This can result in multiple <b>OnContentUpdated</b> calls. 




## -see-also




<a href="https://msdn.microsoft.com/3594011a-da4a-4550-9b3b-076218d09f39">IDirectManipulationViewportEventHandler</a>
 

 

