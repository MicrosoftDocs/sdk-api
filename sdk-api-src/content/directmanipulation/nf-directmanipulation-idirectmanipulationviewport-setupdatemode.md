---
UID: NF:directmanipulation.IDirectManipulationViewport.SetUpdateMode
title: IDirectManipulationViewport::SetUpdateMode (directmanipulation.h)
description: Specifies whether a viewport updates content manually instead of during an input event.
old-location: directmanipulation\idirectmanipulationviewport_setupdatemode.htm
tech.root: directmanipulation
ms.assetid: 10516474-f3ef-4de7-a5b5-aabaa5c65cf5
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetUpdateMode method, IDirectManipulationViewport.SetUpdateMode, IDirectManipulationViewport::SetUpdateMode, SetUpdateMode, SetUpdateMode method [Direct Manipulation], SetUpdateMode method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setupdatemode, directmanipulation/IDirectManipulationViewport::SetUpdateMode
ms.topic: method
f1_keywords:
- directmanipulation/IDirectManipulationViewport.SetUpdateMode
dev_langs:
- c++
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
- IDirectManipulationViewport.SetUpdateMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationViewport::SetUpdateMode


## -description


    Specifies whether a viewport updates content manually instead of during an input event.


## -parameters




### -param mode [in]

One of the values from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_input_mode">DIRECTMANIPULATION_INPUT_MODE</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC is the default mode for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>. In this mode, visual updates are pushed to compositor driven by input. This is the expected mode of operation if the application is using system-provided implementation of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>.


If the application provides its own implementation of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>, it should switch viewport update mode to manual by setting DIRECTMANIPULATION_INPUT_MODE_MANUAL. When in manual mode, the compositor pulls visual updates whenever it calls <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatemanager-update">Update</a> on <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.


Calling this method with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_input_mode">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> set is similar to calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportoptions">SetViewportOptions(DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT)</a>. However, calling <b>SetViewportOptions</b> also overrides all other settings.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>
 

 

