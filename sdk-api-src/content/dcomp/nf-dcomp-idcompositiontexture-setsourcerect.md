---
UID: NF:dcomp.IDCompositionTexture.SetSourceRect
title: IDCompositionTexture::SetSourceRect
description: Specifies the region of a Direct3D texture that the composition texture represents.
tech.root: directcomp
ms.date: 06/09/2023
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
 - IDCompositionTexture::SetSourceRect
f1_keywords:
 - IDCompositionTexture::SetSourceRect
 - dcomp/IDCompositionTexture::SetSourceRect
dev_langs:
 - c++
helpviewer_keywords:
 - SetSourceRect
---

## -description

Specifies the portion of an overall Direct3D texture that the composition texture represents (and samples from). This allows you to have multiple composition textures referencing the same Direct3D texture.

## -parameters

### -param sourceRect

Type: \_In\_ **[D2D_RECT_U](/windows/win32/api/dcommon/ns-dcommon-d2d_rect_u)\&**

The region of a Direct3D texture that the composition texture represents.

## -returns

Type: **[HRESULT](/windows/win32/winprog/windows-data-types)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/winprog/windows-data-types) error code.

## -remarks

## -see-also

* [IDCompositionTexture interface](./nn-dcomp-idcompositiontexture.md)
* [IDCompositionTexture::GetAvailableFence](./nf-dcomp-idcompositiontexture-getavailablefence.md)
