---
UID: NN:dcomp.IDCompositionTexture
title: IDCompositionTexture
description: The interface to an object that represents a raw Direct3D texture that can be bound to a DComp visual as content.
tech.root: directcomp
ms.date: 06/09/2023
targetos: Windows
prerelease: true
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: dcomp.h
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
 - dcomp.h
api_name:
 - IDCompositionTexture
f1_keywords:
 - IDCompositionTexture
 - dcomp/IDCompositionTexture
dev_langs:
 - c++
helpviewer_keywords:
 - IDCompositionTexture
---

## -description

The interface to an object that represents a raw Direct3D texture that can be bound to a composition visual as content. The object can be used anywhere that a generic composition surface can be used in those APIs today&mdash;for example, as the content of a sprite visual or a surface brush. The object exposes an available fence, which can be used to synchronize application rendering and composition work. Can also accept various attributes, such as an alpha mode, source rect, and color space, to more precisely define the content being displayed.

The composition textures API supports Direct3D 11 only.

## -inheritance

The **IDCompositionTexture** interface derives from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.

## -remarks

The lifetime of a composition texture is designed to work without intervention from your app. Your app doesn't need to keep a texture alive for the sake of what the system might be doing. If your app releases a texture that the system is still displaying in a visual tree, then the system will keep that texture alive until it's no longer necessary to do so. Your app can operate under the assumption that it needs to keep a composition texture alive only if it wants to explicitly reference it again.

## -see-also
