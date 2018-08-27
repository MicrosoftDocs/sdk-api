---
UID: NF:directmanipulation.IDirectManipulationViewport.SetManualGesture
title: IDirectManipulationViewport::SetManualGesture
author: windows-sdk-content
description: Sets which gestures are ignored by Direct Manipulation.
old-location: directmanipulation\idirectmanipulationviewport_setmanualgesture.htm
old-project: directmanipulation
ms.assetid: EBBBCEDB-8BAC-4E87-A69C-9730865A257F
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetManualGesture method, IDirectManipulationViewport.SetManualGesture, IDirectManipulationViewport::SetManualGesture, SetManualGesture, SetManualGesture method [Direct Manipulation], SetManualGesture method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setmanualgesture, directmanipulation/IDirectManipulationViewport::SetManualGesture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.SetManualGesture
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::SetManualGesture


## -description


Sets which gestures are ignored by <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. 


## -parameters




### -param configuration [in]

One of the values from <a href="https://msdn.microsoft.com/B8EE991B-6DBF-42DE-966F-FA5CB397562C">DIRECTMANIPULATION_GESTURE_CONFIGURATION</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Use this method to specify which gestures the application processes on the UI thread. If a gesture is recognized, it will be passed to the application for processing and ignored by <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>.


#### Examples

The following example shows how zoom gestures can be ignored by <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> and handled by the application, which may have custom zoom behavior implementation.


```
HRESULT hr = pViewport->SetManualGesture(DIRECTMANIPULATION_GESTURE_PINCH_ZOOM);
```





## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

