---
UID: NF:dcomp.IDCompositionTexture.SetAlphaMode
title: IDCompositionTexture::SetAlphaMode
description: Informs the DWM whether alpha pixels in the texture should be honored or ignored.
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
 - IDCompositionTexture::SetAlphaMode
f1_keywords:
 - IDCompositionTexture::SetAlphaMode
 - dcomp/IDCompositionTexture::SetAlphaMode
dev_langs:
 - c++
helpviewer_keywords:
 - SetAlphaMode
---

## -description

Informs the [Desktop Window Manager (DWM)](/windows/win32/dwm/dwm-overview) whether alpha pixels in the texture should be honored or ignored.

## -parameters

### -param alphaMode

Type: \_In\_ **[DXGI_ALPHA_MODE](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode)**

Indicates whether alpha pixels in the texture should be honored or ignored.

| Value | Meaning |
| - | - |
| **DXGI_ALPHA_MODE_UNSPECIFIED** | The alpha channel isn't specified. This value has the same effect as **DXGI_ALPHA_MODE_IGNORE**. |
| **DXGI_ALPHA_MODE_PREMULTIPLIED** | The color channels contain values that are premultiplied with the alpha channel. |
| **DXGI_ALPHA_MODE_IGNORE** | The alpha channel should be ignored, and the bitmap should be rendered opaquely. |

## -returns

Type: **[HRESULT](/windows/win32/winprog/windows-data-types)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/winprog/windows-data-types) error code.

## -remarks

## -see-also

* [IDCompositionTexture interface](./nn-dcomp-idcompositiontexture.md)
