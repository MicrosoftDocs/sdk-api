---
UID: NF:directmanipulation.IDirectManipulationViewportEventHandler.OnContentUpdated
title: IDirectManipulationViewportEventHandler::OnContentUpdated
author: windows-sdk-content
description: Called when content inside a viewport is updated.
old-location: directmanipulation\idirectmanipulationviewporteventhandler_oncontentupdated.htm
old-project: directmanipulation
ms.assetid: 1b9a0f54-ccc7-4927-a34e-724652f6c2f0
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationViewportEventHandler interface [Direct Manipulation],OnContentUpdated method, IDirectManipulationViewportEventHandler.OnContentUpdated, IDirectManipulationViewportEventHandler::OnContentUpdated, OnContentUpdated, OnContentUpdated method [Direct Manipulation], OnContentUpdated method [Direct Manipulation],IDirectManipulationViewportEventHandler interface, directmanipulation.idirectmanipulationviewporteventhandler_oncontentupdated, directmanipulation/IDirectManipulationViewportEventHandler::OnContentUpdated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	directmanipulation.h
api_name:
-	IDirectManipulationViewportEventHandler.OnContentUpdated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

