---
UID: NF:directmanipulation.IDirectManipulationViewport.Stop
title: IDirectManipulationViewport::Stop
author: windows-driver-content
description: Stops the manipulation and returns the viewport to a ready state.
old-location: directmanipulation\idirectmanipulationviewport_stop.htm
old-project: directmanipulation
ms.assetid: e0b88429-0d75-4c4a-8468-1a5637455324
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],Stop method, IDirectManipulationViewport.Stop, IDirectManipulationViewport::Stop, Stop, Stop method [Direct Manipulation], Stop method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_stop, directmanipulation/IDirectManipulationViewport::Stop
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
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationViewport.Stop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::Stop


## -description


    Stops the manipulation and returns the viewport to a ready state.  



## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If a mandatory snap point has been configured, the content may animate to the nearest snap point.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

