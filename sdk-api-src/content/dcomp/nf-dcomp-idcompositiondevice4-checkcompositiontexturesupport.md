---
UID: NF:dcomp.IDCompositionDevice4.CheckCompositionTextureSupport
title: IDCompositionDevice4::CheckCompositionTextureSupport
description: Queries whether the Direct3D device that you're using to render supports composition textures.
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
 - IDCompositionDevice4::CheckCompositionTextureSupport
f1_keywords:
 - IDCompositionDevice4::CheckCompositionTextureSupport
 - dcomp/IDCompositionDevice4::CheckCompositionTextureSupport
dev_langs:
 - c++
helpviewer_keywords:
 - CheckCompositionTextureSupport
---

## -description

Queries whether the Direct3D device that you're using to render supports composition textures (without having to first allocate a Direct3D texture on that device). Before you attempt to create composition textures for Direct3D textures backed by a given Direct3D device, you should call **CheckCompositionTextureSupport**, passing that backing device.

Generally speaking, a rendering device that reports support for either monitored or non-monitored fences via [DXGI_ADAPTER_FLAG3](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) is able to support composition textures. But in rare cases, the operating system (OS) itself can disable the composition textures feature; in which case **CheckCompositionTextureSupport** will also report unsupported.

## -parameters

### -param renderingDevice

Type: \_In\_ **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

The backing Direct3D device.

### -param supportsCompositionTextures

Type: \_Out\_ **[BOOL](/windows/win32/winprog/windows-data-types)\***

Points to a value of `true` if *renderingDevice* supports composition textures; otherwise `false`.

## -returns

Type: **[HRESULT](/windows/win32/winprog/windows-data-types)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/winprog/windows-data-types) error code.

## -remarks

## -see-also

* [IDCompositionDevice4 interface](./nn-dcomp-idcompositiondevice4.md)
