---
UID: NF:directmanipulation.IDirectManipulationViewport.SetUpdateMode
title: IDirectManipulationViewport::SetUpdateMode
author: windows-sdk-content
description: Specifies whether a viewport updates content manually instead of during an input event.
old-location: directmanipulation\idirectmanipulationviewport_setupdatemode.htm
old-project: directmanipulation
ms.assetid: 10516474-f3ef-4de7-a5b5-aabaa5c65cf5
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetUpdateMode method, IDirectManipulationViewport.SetUpdateMode, IDirectManipulationViewport::SetUpdateMode, SetUpdateMode, SetUpdateMode method [Direct Manipulation], SetUpdateMode method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setupdatemode, directmanipulation/IDirectManipulationViewport::SetUpdateMode
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
 - IDirectManipulationViewport.SetUpdateMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::SetUpdateMode


## -description


    Specifies whether a viewport updates content manually instead of during an input event.


## -parameters




### -param mode [in]

One of the values from <a href="https://msdn.microsoft.com/92839109-91d5-45fc-85d0-dc5a14e4ebf0">DIRECTMANIPULATION_INPUT_MODE</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC is the default mode for <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. In this mode, visual updates are pushed to compositor driven by input. This is the expected mode of operation if the application is using system-provided implementation of <a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>.


If the application provides its own implementation of <a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>, it should switch viewport update mode to manual by setting DIRECTMANIPULATION_INPUT_MODE_MANUAL. When in manual mode, the compositor pulls visual updates whenever it calls <a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a> on <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>.


Calling this method with <a href="https://msdn.microsoft.com/92839109-91d5-45fc-85d0-dc5a14e4ebf0">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> set is similar to calling <a href="https://msdn.microsoft.com/F2B861B9-9E86-4AEE-B86C-03BF37F0988B">SetViewportOptions(DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT)</a>. However, calling <b>SetViewportOptions</b> also overrides all other settings.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

