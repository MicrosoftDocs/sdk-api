---
UID: NF:directmanipulation.IDirectManipulationViewport.SetViewportOptions
title: IDirectManipulationViewport::SetViewportOptions (directmanipulation.h)
description: Sets how the viewport handles input and output.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","SetViewportOptions method","IDirectManipulationViewport.SetViewportOptions","IDirectManipulationViewport::SetViewportOptions","SetViewportOptions","SetViewportOptions method [Direct Manipulation]","SetViewportOptions method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_setviewportoptions","directmanipulation/IDirectManipulationViewport::SetViewportOptions"]
old-location: directmanipulation\idirectmanipulationviewport_setviewportoptions.htm
tech.root: directmanipulation
ms.assetid: F2B861B9-9E86-4AEE-B86C-03BF37F0988B
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetViewportOptions method, IDirectManipulationViewport.SetViewportOptions, IDirectManipulationViewport::SetViewportOptions, SetViewportOptions, SetViewportOptions method [Direct Manipulation], SetViewportOptions method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setviewportoptions, directmanipulation/IDirectManipulationViewport::SetViewportOptions
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
 - IDirectManipulationViewport::SetViewportOptions
 - directmanipulation/IDirectManipulationViewport::SetViewportOptions
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
 - IDirectManipulationViewport.SetViewportOptions
---

# IDirectManipulationViewport::SetViewportOptions


## -description

Sets how the viewport handles input and output.

Calling this method overrides all  settings previously specified with <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setupdatemode">SetUpdateMode</a> or <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setinputmode">SetInputMode</a>.

## -parameters

### -param options [in]

One or more of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_viewport_options">DIRECTMANIPULATION_VIEWPORT_OPTIONS</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling this method with <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_input_mode">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> set is similar to calling <b>SetViewportOptions(DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT)</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>