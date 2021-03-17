---
UID: NF:directmanipulation.IDirectManipulationViewport.GetViewportRect
title: IDirectManipulationViewport::GetViewportRect (directmanipulation.h)
description: Retrieves the rectangle for the viewport relative to the origin of the viewport coordinate system specified by SetViewportRect.
helpviewer_keywords: ["GetViewportRect","GetViewportRect method [Direct Manipulation]","GetViewportRect method [Direct Manipulation]","IDirectManipulationViewport interface","IDirectManipulationViewport interface [Direct Manipulation]","GetViewportRect method","IDirectManipulationViewport.GetViewportRect","IDirectManipulationViewport::GetViewportRect","directmanipulation.idirectmanipulationviewport_getviewportrect","directmanipulation/IDirectManipulationViewport::GetViewportRect"]
old-location: directmanipulation\idirectmanipulationviewport_getviewportrect.htm
tech.root: directmanipulation
ms.assetid: 0d20e7f7-aa2a-4c76-a3ff-da10d4dec3ea
ms.date: 12/05/2018
ms.keywords: GetViewportRect, GetViewportRect method [Direct Manipulation], GetViewportRect method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],GetViewportRect method, IDirectManipulationViewport.GetViewportRect, IDirectManipulationViewport::GetViewportRect, directmanipulation.idirectmanipulationviewport_getviewportrect, directmanipulation/IDirectManipulationViewport::GetViewportRect
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
 - IDirectManipulationViewport::GetViewportRect
 - directmanipulation/IDirectManipulationViewport::GetViewportRect
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
 - IDirectManipulationViewport.GetViewportRect
---

# IDirectManipulationViewport::GetViewportRect


## -description

Retrieves the rectangle for the viewport relative to the origin of the viewport coordinate system specified by <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect">SetViewportRect</a>.

## -parameters

### -param viewport [out, retval]

The bounding rectangle relative to the viewport coordinate system.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>