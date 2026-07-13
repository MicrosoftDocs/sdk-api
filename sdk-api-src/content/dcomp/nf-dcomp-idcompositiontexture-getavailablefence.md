---
UID: NF:dcomp.IDCompositionTexture.GetAvailableFence
title: IDCompositionTexture::GetAvailableFence
description: Retrieves a Direct3D synchronization fence/value pair that indicates when the composition texture will become available, if that info is known.
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
 - IDCompositionTexture::GetAvailableFence
f1_keywords:
 - IDCompositionTexture::GetAvailableFence
 - dcomp/IDCompositionTexture::GetAvailableFence
dev_langs:
 - c++
helpviewer_keywords:
 - GetAvailableFence
---

## -description

Retrieves a Direct3D synchronization fence/value pair that indicates when the composition texture will become available, if that info is known. The value returned depends on the availability state of the composition texture. An availability state specifies whether, and when, it's safe to render to the composition texture.

See the **Remarks** section for the availability states, their descriptions, and how **GetAvailableFence** behaves for each state.

If a composition texture becomes available, then your app must be careful to issue rendering only to the exact subregion of the Direct3D texture that it refers to.

## -parameters

### -param fenceValue

Type: \_Out\_ **UINT64\***

The returned fence value.

### -param iid

Type: \_In\_ **REFIID**

An interface identifier.

### -param availableFence

Type: \_Outptr\_result\_maybenull\_ **void\*\***

The returned available fence, or `nullptr`, depending on the availability state of the composition texture. For details, see the **Remarks** section.

## -returns

Type: **[HRESULT](/windows/win32/winprog/windows-data-types)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/winprog/windows-data-types) error code.

## -remarks

Here are the availability states, their descriptions, and how **GetAvailableFence** behaves for each state.

**immediately available**. The composition texture isn't being displayed by the desktop window manager (DWM), nor are application commits queued to have it do so. So the composition texture is safe to write to immediately. **GetAvailableFence** returns the available fence, which will already match the returned value.

**soon-to-be available**. The composition texture is currently being displayed by DWM, but the application has removed it from its visual tree, and committed to DWM. However, that commit hasn't yet been processed by DWM, so DWM hasn't yet stopped displaying the texture. Your app can render to a soon-to-be available texture if that work is synchronized against the texture’s available fence. **GetAvailableFence** returns the available fence. The composition texture will be safe to write to when that fence is signaled to the returned value.

**unavailable**. The composition texture is currently being displayed by DWM, or it's queued for display by DWM. So your app shouldn't write to it. **GetAvailableFence** returns `nullptr` instead of a fence.

The available fence describes the availability of a single composition texture. Multiple composition textures might reference the same Direct3D texture, if each composition texture takes a different (non-overlapping) region of the larger Direct3D texture by specifying a source rect (a technique known as atlasing). In a case like that, if a composition texture becomes available, then your app must be careful to issue rendering only to the exact subregion of the Direct3D texture; to make sure not to interfere with pixels that might belong to other composition textures (which might not be available). That's because different regions of a single Direct3D texture might have different availability states.

## -see-also

* [IDCompositionTexture interface](./nn-dcomp-idcompositiontexture.md)
