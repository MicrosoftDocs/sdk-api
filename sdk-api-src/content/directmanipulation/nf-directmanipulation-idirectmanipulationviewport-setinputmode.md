---
UID: NF:directmanipulation.IDirectManipulationViewport.SetInputMode
title: IDirectManipulationViewport::SetInputMode
author: windows-sdk-content
description: Specifies if input is visible to the UI thread.
old-location: directmanipulation\idirectmanipulationviewport_setinputmode.htm
tech.root: directmanipulation
ms.assetid: 2be1c8a1-a729-4851-b103-b108b9a96e2d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetInputMode method, IDirectManipulationViewport.SetInputMode, IDirectManipulationViewport::SetInputMode, SetInputMode, SetInputMode method [Direct Manipulation], SetInputMode method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setinputmode, directmanipulation/IDirectManipulationViewport::SetInputMode
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.SetInputMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::SetInputMode


## -description


Specifies if input is visible to the UI thread.


## -parameters




### -param mode [in]

One of the values from <a href="https://msdn.microsoft.com/92839109-91d5-45fc-85d0-dc5a14e4ebf0">DIRECTMANIPULATION_INPUT_MODE</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC is the default mode for <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. 


<a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> consumes all the input that drives the manipulation and the application receives WM_POINTERCAPTURECHANGED messages. 


In some situations an application may want to receive input that is driving a manipulation. Set DIRECTMANIPULATION_INPUT_MODE_MANUAL in this case. The application will receive all input messages, even input used by <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> to drive a manipulation. 

<div class="alert"><b>Note</b>  The application will not receive WM_POINTERCAPTURECHANGED messages.
</div>
<div> </div>
Calling this method with <a href="https://msdn.microsoft.com/92839109-91d5-45fc-85d0-dc5a14e4ebf0">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> set is similar to calling <a href="https://msdn.microsoft.com/F2B861B9-9E86-4AEE-B86C-03BF37F0988B">SetViewportOptions(DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT)</a>. However, calling <b>SetViewportOptions</b> also overrides all other settings.


#### Examples

The following example shows how to use this method.


```
HRESULT hr = pViewport->SetInputMode(DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC);
```





## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

