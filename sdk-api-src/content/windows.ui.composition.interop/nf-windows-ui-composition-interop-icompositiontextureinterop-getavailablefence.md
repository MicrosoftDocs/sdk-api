---
UID: NF:windows.ui.composition.interop.ICompositionTextureInterop.GetAvailableFence
title: ICompositionTextureInterop::GetAvailableFence
description: Retrieves a Direct3D synchronization fence/value pair that indicates when the composition texture will become available, if that info is known.
tech.root: winrt
ms.date: 07/10/2023
targetos: Windows
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windows.ui.composition.interop.h
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
 - windows.ui.composition.interop.h
api_name:
 - ICompositionTextureInterop::GetAvailableFence
f1_keywords:
 - ICompositionTextureInterop::GetAvailableFence
 - windows.ui.composition.interop/ICompositionTextureInterop::GetAvailableFence
dev_langs:
 - c++
helpviewer_keywords:
 - GetAvailableFence
---

## -description

Retrieves a Direct3D synchronization fence/value pair that indicates when the composition texture will become available, if that info is known. The value returned depends on the availability state of the composition texture. An availability state specifies whether, and when, it's safe to render to the composition texture.

See the **Remarks** section of [IDCompositionTexture::GetAvailableFence](../dcomp/nf-dcomp-idcompositiontexture-getavailablefence.md) for the availability states, their descriptions, and how **GetAvailableFence** behaves for each state.

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

The returned available fence, or `nullptr`, depending on the availability state of the composition texture. For details, see the **Remarks** section of [IDCompositionTexture::GetAvailableFence](../dcomp/nf-dcomp-idcompositiontexture-getavailablefence.md).

## -returns

Type: **[HRESULT](/windows/win32/winprog/windows-data-types)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/winprog/windows-data-types) error code.

## -remarks

## -see-also

* [ICompositionTextureInterop interface](./nn-windows-ui-composition-interop-icompositiontextureinterop.md)
* [IDCompositionTexture::GetAvailableFence](../dcomp/nf-dcomp-idcompositiontexture-getavailablefence.md)
