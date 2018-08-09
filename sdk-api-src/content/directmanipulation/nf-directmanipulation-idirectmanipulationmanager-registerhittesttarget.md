---
UID: NF:directmanipulation.IDirectManipulationManager.RegisterHitTestTarget
title: IDirectManipulationManager::RegisterHitTestTarget
author: windows-sdk-content
description: Registers a dedicated thread for hit testing.
old-location: directmanipulation\idirectmanipulationmanager_registerhittesttarget.htm
old-project: directmanipulation
ms.assetid: ba71a959-b9b9-4466-9239-f3c486f5e7b3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDirectManipulationManager interface [Direct Manipulation],RegisterHitTestTarget method, IDirectManipulationManager.RegisterHitTestTarget, IDirectManipulationManager::RegisterHitTestTarget, RegisterHitTestTarget, RegisterHitTestTarget method [Direct Manipulation], RegisterHitTestTarget method [Direct Manipulation],IDirectManipulationManager interface, directmanipulation.idirectmanipulationmanager_registerhittesttarget, directmanipulation/IDirectManipulationManager::RegisterHitTestTarget
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager.RegisterHitTestTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationManager::RegisterHitTestTarget


## -description


Registers a dedicated thread for hit testing.


## -parameters




### -param window [in]

The handle of the main app window (typically created from the UI thread).


### -param hitTestWindow [in, optional]

The handle of the window in which hit testing is registered (should be created from the hit testing thread). Pass in nullptr to unregister a previously registered hit-test target.


### -param type [in]

One of the values from <a href="https://msdn.microsoft.com/68e65695-9f28-4da4-9080-4030ed10c6ed">DIRECTMANIPULATION_HITTEST_TYPE</a>. Specifies whether the UI window or the hit testing window (or both) receives the hit testing <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> message , and in what order.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Hit testing is typically performed on the application UI thread. The application receives a <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> message on which hit-testing is performed. If a manipulation is required, <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> is called on one or more viewports. An application can use the <b>RegisterHitTestTarget</b> method to delegate this hit-testing responsibility to a separate hit-testing thread.


Once a dedicated hit-test target is successfully registered, <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages are processed on the hit-testing thread. If a manipulation, such as pan or zoom, is required, <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> is called from this thread.


If <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> is not called from the hit-testing thread, <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages may be processed on the UI thread, depending on the <a href="https://msdn.microsoft.com/68e65695-9f28-4da4-9080-4030ed10c6ed">DIRECTMANIPULATION_HITTEST_TYPE</a> specified during registration.


If <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> is not called by either the hit-test thread or the UI thread, <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> ignores the input which is then handled on the UI thread.





## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

