---
UID: NF:directmanipulation.IDirectManipulationViewportEventHandler.OnViewportStatusChanged
title: IDirectManipulationViewportEventHandler::OnViewportStatusChanged method
author: windows-driver-content
description: Called when the status of a viewport changes.
old-location: directmanipulation\idirectmanipulationviewporteventhandler_onviewportstatuschanged.htm
old-project: directmanipulation
ms.assetid: 7fe7106d-1b13-4a3e-8841-550e0ef55f95
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDirectManipulationViewportEventHandler, IDirectManipulationViewportEventHandler interface [Direct Manipulation], OnViewportStatusChanged method, IDirectManipulationViewportEventHandler::OnViewportStatusChanged, OnViewportStatusChanged method [Direct Manipulation], OnViewportStatusChanged method [Direct Manipulation], IDirectManipulationViewportEventHandler interface, OnViewportStatusChanged,IDirectManipulationViewportEventHandler.OnViewportStatusChanged, directmanipulation.idirectmanipulationviewporteventhandler_onviewportstatuschanged, directmanipulation/IDirectManipulationViewportEventHandler::OnViewportStatusChanged
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
-	directmanipulation.h
api_name:
-	IDirectManipulationViewportEventHandler.OnViewportStatusChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewportEventHandler::OnViewportStatusChanged method


## -description


Called when the status of a viewport changes.


## -parameters




### -param viewport [in]

The viewport for which status has changed.


### -param current [in]

The new status of the viewport.


### -param previous [in]

The previous status of the viewport.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If you call <a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a> from within this handler, the status returned is not guaranteed to be the same as at the time of the call. This is because of the asynchronous nature of the notification.




## -see-also




<a href="https://msdn.microsoft.com/3594011a-da4a-4550-9b3b-076218d09f39">IDirectManipulationViewportEventHandler</a>
 

 

