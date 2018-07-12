---
UID: NF:directmanipulation.IDirectManipulationViewport.SetViewportOptions
title: IDirectManipulationViewport::SetViewportOptions
author: windows-sdk-content
description: Sets how the viewport handles input and output.
old-location: directmanipulation\idirectmanipulationviewport_setviewportoptions.htm
old-project: directmanipulation
ms.assetid: F2B861B9-9E86-4AEE-B86C-03BF37F0988B
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetViewportOptions method, IDirectManipulationViewport.SetViewportOptions, IDirectManipulationViewport::SetViewportOptions, SetViewportOptions, SetViewportOptions method [Direct Manipulation], SetViewportOptions method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setviewportoptions, directmanipulation/IDirectManipulationViewport::SetViewportOptions
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
 - IDirectManipulationViewport.SetViewportOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::SetViewportOptions


## -description


Sets how the viewport handles input and output.

Calling this method overrides all  settings previously specified with <a href="https://msdn.microsoft.com/10516474-f3ef-4de7-a5b5-aabaa5c65cf5">SetUpdateMode</a> or <a href="https://msdn.microsoft.com/2be1c8a1-a729-4851-b103-b108b9a96e2d">SetInputMode</a>.


## -parameters




### -param options [in]

One or more of the values from <a href="https://msdn.microsoft.com/BFBA2D32-825F-4EEF-99C8-291305926750">DIRECTMANIPULATION_VIEWPORT_OPTIONS</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Calling this method with <a href="https://msdn.microsoft.com/92839109-91d5-45fc-85d0-dc5a14e4ebf0">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> set is similar to calling <b>SetViewportOptions(DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT)</b>.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

