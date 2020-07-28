---
UID: NN:windows.ui.composition.interop.ICompositionDrawingSurfaceInterop2
title: interop::ICompositionDrawingSurfaceInterop2
description: A native interoperation interface that allows you to read back the contents of a composition drawing surface (or a composition virtual drawing surface).
ms.date: 01/07/2020
tech.root: winrt
ms.topic: language-reference
f1_keywords:
 - windows/interop::ICompositionDrawingSurfaceInterop2
dev_langs:
- c++
req.construct-type: iface
req.header: windows.ui.composition.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
topic_type:
 - apiref
api_type:
- COM
api_location:
- windows.ui.composition.interop.h
api_name:
 - interop::ICompositionDrawingSurfaceInterop2
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

A native interoperation interface that allows you to read back the contents of a composition drawing surface (or a composition virtual drawing surface). This interface is available in C++ only.

**ICompositionDrawingSurfaceInterop2** inherits from the [ICompositionDrawingSurfaceInterop](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) interface.

## -remarks

> [!NOTE]
> This interface is available on Windows 10, version 1903 (10.0; Build 18362), but it is not defined in the `windows.ui.composition.interop.h` header file for that version of the Windows Software Development Kit (SDK). If you first obtain a pointer to an [ICompositionDrawingSurfaceInterop](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) interface, you can then query that (via [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))) for a pointer to an **ICompositionDrawingSurfaceInterop2** interface.

## -see-also

[ICompositionDrawingSurfaceInterop interface](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop)

[Composition native interoperation overview](/windows/uwp/composition/composition-native-interop)
