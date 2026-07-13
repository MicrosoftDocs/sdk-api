---
UID: NF:dcomp.IDCompositionTexture.SetColorSpace
title: IDCompositionTexture::SetColorSpace
description: Informs the system of the color space that it should map the texture into.
tech.root: directcomp
ms.date: 07/10/2023
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
 - IDCompositionTexture::SetColorSpace
f1_keywords:
 - IDCompositionTexture::SetColorSpace
 - dcomp/IDCompositionTexture::SetColorSpace
dev_langs:
 - c++
helpviewer_keywords:
 - SetColorSpace
---

## -description

Informs the system of the color space that it should map the texture into.

## -parameters

### -param colorSpace

Type: \_In\_ **[DXGI_COLOR_SPACE_TYPE](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)**

Specifies the color space to use.

## -returns

Type: **[HRESULT](/windows/win32/winprog/windows-data-types)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/winprog/windows-data-types) error code.

## -remarks

## -see-also

* [IDCompositionTexture interface](./nn-dcomp-idcompositiontexture.md)
