---
UID: NF:directmanipulation.IDirectManipulationViewport.SetViewportRect
title: IDirectManipulationViewport::SetViewportRect (directmanipulation.h)
description: Sets the bounding rectangle for the viewport, relative to the origin of the viewport coordinate system.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","SetViewportRect method","IDirectManipulationViewport.SetViewportRect","IDirectManipulationViewport::SetViewportRect","SetViewportRect","SetViewportRect method [Direct Manipulation]","SetViewportRect method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_setviewportrect","directmanipulation/IDirectManipulationViewport::SetViewportRect"]
old-location: directmanipulation\idirectmanipulationviewport_setviewportrect.htm
tech.root: directmanipulation
ms.assetid: 45dfdf6e-aa4d-489a-bf9a-016e42eb57f6
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetViewportRect method, IDirectManipulationViewport.SetViewportRect, IDirectManipulationViewport::SetViewportRect, SetViewportRect, SetViewportRect method [Direct Manipulation], SetViewportRect method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setviewportrect, directmanipulation/IDirectManipulationViewport::SetViewportRect
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
 - IDirectManipulationViewport::SetViewportRect
 - directmanipulation/IDirectManipulationViewport::SetViewportRect
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
 - IDirectManipulationViewport.SetViewportRect
---

# IDirectManipulationViewport::SetViewportRect


## -description

    Sets the bounding rectangle for the viewport, relative to the origin of the viewport coordinate system.

## -parameters

### -param viewport [in]

The bounding rectangle.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The viewport rectangle specifies the region of content that is visible to the user. In conjunction with the primary content rectangle, the viewport rectangle is used to determine chaining behaviors.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>