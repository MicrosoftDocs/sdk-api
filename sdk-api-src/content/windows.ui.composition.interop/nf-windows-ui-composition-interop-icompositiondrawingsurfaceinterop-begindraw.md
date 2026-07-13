---
UID: NF:windows.ui.composition.interop.ICompositionDrawingSurfaceInterop.BeginDraw
title: ICompositionDrawingSurfaceInterop::BeginDraw (windows.ui.composition.interop.h)
description: Initiates drawing on the surface.
helpviewer_keywords: ["BeginDraw","BeginDraw method","BeginDraw method","ICompositionDrawingSurfaceInterop interface","ICompositionDrawingSurfaceInterop interface","BeginDraw method","ICompositionDrawingSurfaceInterop.BeginDraw","ICompositionDrawingSurfaceInterop.composition","ICompositionDrawingSurfaceInterop::BeginDraw","ICompositionDrawingSurfaceInterop::composition","w_ui_comp.icompositiondrawingsurfaceinterop_begindraw","windows/ICompositionDrawingSurfaceInterop::BeginDraw"]
old-location: w_ui_comp\icompositiondrawingsurfaceinterop_begindraw.htm
tech.root: winrt
ms.assetid: 01273B2A-0305-4F1E-8461-7956EDD651A7
ms.date: 12/05/2018
ms.keywords: BeginDraw, BeginDraw method, BeginDraw method,ICompositionDrawingSurfaceInterop interface, ICompositionDrawingSurfaceInterop interface,BeginDraw method, ICompositionDrawingSurfaceInterop.BeginDraw, ICompositionDrawingSurfaceInterop.composition, ICompositionDrawingSurfaceInterop::BeginDraw, ICompositionDrawingSurfaceInterop::composition, w_ui_comp.icompositiondrawingsurfaceinterop_begindraw, windows/ICompositionDrawingSurfaceInterop::BeginDraw
req.header: windows.ui.composition.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ICompositionDrawingSurfaceInterop::BeginDraw
 - windows.ui.composition.interop/ICompositionDrawingSurfaceInterop::BeginDraw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositionDrawingSurfaceInterop.BeginDraw
---

# ICompositionDrawingSurfaceInterop::BeginDraw (windows.ui.composition.interop.h)


## -description

Initiates drawing on the surface.

## -parameters

### -param updateRect [in, optional]

Type: <b>const RECT*</b>

The section of the surface to update. The update rectangle must be within the boundaries of the surface. Specifying nullptr indicates the entire surface should be updated.

### -param iid [in]

Type: <b>REFIID</b>

The identifier of the interface to retrieve.

### -param updateObject [out]

Type: <b>void**</b>

Receives an interface pointer of the type specified in the iid parameter. This parameter must not be NULL.

### -param updateOffset [out]

Type: <b>POINT*</b>

The offset into the surface where the application should draw updated content. This offset will reference the upper left corner of the update rectangle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop">ICompositionDrawingSurfaceInterop</a>
