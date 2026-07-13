---
UID: NN:windows.ui.composition.interop.ICompositionTextureInterop
title: ICompositionTextureInterop
description: TBD
tech.root: winrt
ms.date: 06/15/2023
targetos: Windows
prerelease: true
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: windows.ui.composition.interop.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositionTextureInterop
f1_keywords:
 - ICompositionTextureInterop
 - windows.ui.composition.interop/ICompositionTextureInterop
dev_langs:
 - c++
helpviewer_keywords:
 - ICompositionTextureInterop
---

## -description

To access interop methods, query **ICompositionTextureInterop** from the composition texture object.

The interface to an object that represents a raw Direct3D texture that can be bound to a DComp visual as content. The object can be used anywhere that a generic composition surface can be used in those APIs today&mdash;for example, as the content of a visual or a surface brush. The object exposes an available fence, which can be used to synchronize application rendering and composition work. Can also accept various attributes, such as an alpha mode, source rect, and color space, to more precisely define the content being displayed.

The composition textures API supports Direct3D 11 only.

## -remarks

## -see-also
