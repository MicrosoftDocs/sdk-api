---
UID: NF:directmanipulation.IDirectManipulationViewport.SetInputMode
title: IDirectManipulationViewport::SetInputMode (directmanipulation.h)
description: Specifies if input is visible to the UI thread.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","SetInputMode method","IDirectManipulationViewport.SetInputMode","IDirectManipulationViewport::SetInputMode","SetInputMode","SetInputMode method [Direct Manipulation]","SetInputMode method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_setinputmode","directmanipulation/IDirectManipulationViewport::SetInputMode"]
old-location: directmanipulation\idirectmanipulationviewport_setinputmode.htm
tech.root: directmanipulation
ms.assetid: 2be1c8a1-a729-4851-b103-b108b9a96e2d
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetInputMode method, IDirectManipulationViewport.SetInputMode, IDirectManipulationViewport::SetInputMode, SetInputMode, SetInputMode method [Direct Manipulation], SetInputMode method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setinputmode, directmanipulation/IDirectManipulationViewport::SetInputMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationViewport::SetInputMode
 - directmanipulation/IDirectManipulationViewport::SetInputMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.SetInputMode
---

# IDirectManipulationViewport::SetInputMode


## -description

Specifies if input is visible to the UI thread.

## -parameters

### -param mode [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_input_mode">DIRECTMANIPULATION_INPUT_MODE</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC is the default mode for <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>. 


<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> consumes all the input that drives the manipulation and the application receives WM_POINTERCAPTURECHANGED messages. 


In some situations an application may want to receive input that is driving a manipulation. Set DIRECTMANIPULATION_INPUT_MODE_MANUAL in this case. The application will receive all input messages, even input used by <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> to drive a manipulation. 

<div class="alert"><b>Note</b>  The application will not receive WM_POINTERCAPTURECHANGED messages.
</div>
<div> </div>
Calling this method with <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_input_mode">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> set is similar to calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportoptions">SetViewportOptions(DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT)</a>. However, calling <b>SetViewportOptions</b> also overrides all other settings.


#### Examples

The following example shows how to use this method.


```
HRESULT hr = pViewport->SetInputMode(DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC);
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>