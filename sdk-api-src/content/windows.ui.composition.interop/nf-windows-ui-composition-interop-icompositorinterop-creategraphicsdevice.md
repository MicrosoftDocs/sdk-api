---
UID: NF:windows.ui.composition.interop.ICompositorInterop.CreateGraphicsDevice
title: ICompositorInterop::CreateGraphicsDevice (windows.ui.composition.interop.h)
description: Creates a CompositionGraphicsDevice backed by the specified rendering device.
helpviewer_keywords: ["CreateGraphicsDevice","CreateGraphicsDevice method","CreateGraphicsDevice method","ICompositorInterop interface","ICompositorInterop interface","CreateGraphicsDevice method","ICompositorInterop.CreateGraphicsDevice","ICompositorInterop.composition","ICompositorInterop::CreateGraphicsDevice","ICompositorInterop::composition","w_ui_comp.icompositorinterop_creategraphicsdevice","windows/ICompositorInterop::CreateGraphicsDevice"]
old-location: w_ui_comp\icompositorinterop_creategraphicsdevice.htm
tech.root: winrt
ms.assetid: 1B4B3CF2-D2E7-4E11-B203-CB16057450B9
ms.date: 12/05/2018
ms.keywords: CreateGraphicsDevice, CreateGraphicsDevice method, CreateGraphicsDevice method,ICompositorInterop interface, ICompositorInterop interface,CreateGraphicsDevice method, ICompositorInterop.CreateGraphicsDevice, ICompositorInterop.composition, ICompositorInterop::CreateGraphicsDevice, ICompositorInterop::composition, w_ui_comp.icompositorinterop_creategraphicsdevice, windows/ICompositorInterop::CreateGraphicsDevice
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
 - ICompositorInterop::CreateGraphicsDevice
 - windows.ui.composition.interop/ICompositorInterop::CreateGraphicsDevice
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
 - ICompositorInterop.CreateGraphicsDevice
---

# ICompositorInterop::CreateGraphicsDevice (windows.ui.composition.interop.h)


## -description

Creates a CompositionGraphicsDevice backed by the specified rendering device.

## -parameters

### -param renderingDevice [in]

Type: <b>IUnknown*</b>

The rendering device to back the CompositionGraphicsDevice.

### -param result [out]

Type: <b>ICompositionGraphicsDevice**</b>

The created CompositionGraphicsDevice.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositorinterop">ICompositorInterop</a>
