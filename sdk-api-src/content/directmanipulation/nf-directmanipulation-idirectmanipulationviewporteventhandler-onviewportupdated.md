---
UID: NF:directmanipulation.IDirectManipulationViewportEventHandler.OnViewportUpdated
title: IDirectManipulationViewportEventHandler::OnViewportUpdated
author: windows-sdk-content
description: Called after all content in the viewport has been updated.
old-location: directmanipulation\idirectmanipulationviewporteventhandler_onviewportupdated.htm
tech.root: directmanipulation
ms.assetid: dfb70d6f-ce3c-4d39-b7b5-21812ff7e56b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDirectManipulationViewportEventHandler interface [Direct Manipulation],OnViewportUpdated method, IDirectManipulationViewportEventHandler.OnViewportUpdated, IDirectManipulationViewportEventHandler::OnViewportUpdated, OnViewportUpdated, OnViewportUpdated method [Direct Manipulation], OnViewportUpdated method [Direct Manipulation],IDirectManipulationViewportEventHandler interface, directmanipulation.idirectmanipulationviewporteventhandler_onviewportupdated, directmanipulation/IDirectManipulationViewportEventHandler::OnViewportUpdated
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directmanipulation.h
api_name:
 - IDirectManipulationViewportEventHandler.OnViewportUpdated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

