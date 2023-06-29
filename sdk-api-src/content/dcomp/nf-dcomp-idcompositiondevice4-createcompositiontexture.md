---
UID: NF:dcomp.IDCompositionDevice4.CreateCompositionTexture
title: IDCompositionDevice4::CreateCompositionTexture
description: Creates a composition texture referencing the passed-in Direct3D texture.
tech.root: directcomp
ms.date: 06/12/2023
targetos: Windows
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dcomp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dcomp.h
api_name:
 - IDCompositionDevice4::CreateCompositionTexture
f1_keywords:
 - IDCompositionDevice4::CreateCompositionTexture
 - dcomp/IDCompositionDevice4::CreateCompositionTexture
dev_langs:
 - c++
helpviewer_keywords:
 - CreateCompositionTexture
---

## -description

Creates a composition texture referencing the passed-in Direct3D texture.

## -parameters

### -param d3dTexture

Type: \_In\_ **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

A Direct3D texture (an [ID3D11Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) resource) to create a composition texture for.

### -param compositionTexture

Type: \_In\_ **[IDCompositionTexture](./nn-dcomp-idcompositiontexture.md)\*\***

Retrieves the composition texture object.

## -returns

Type: **[HRESULT](/windows/win32/winprog/windows-data-types)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/winprog/windows-data-types) error code. If you try to create a composition texture for a Direct3D texture that's backed by a Direct3D device that doesn't support composition textures, then **CreateCompositionTexture** returns **E_INVALIDARG**.

## -remarks

## -see-also

* [IDCompositionDevice4 interface](./nn-dcomp-idcompositiondevice4.md)
* [IDCompositionTexture interface](./nn-dcomp-idcompositiontexture.md)
