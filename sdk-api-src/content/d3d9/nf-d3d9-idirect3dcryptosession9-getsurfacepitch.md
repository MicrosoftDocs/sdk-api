---
UID: NF:d3d9.IDirect3DCryptoSession9.GetSurfacePitch
title: IDirect3DCryptoSession9::GetSurfacePitch (d3d9.h)
description: Gets the stride of a protected surface.
helpviewer_keywords: ["GetSurfacePitch","GetSurfacePitch method [Media Foundation]","GetSurfacePitch method [Media Foundation]","IDirect3DCryptoSession9 interface","IDirect3DCryptoSession9 interface [Media Foundation]","GetSurfacePitch method","IDirect3DCryptoSession9.GetSurfacePitch","IDirect3DCryptoSession9::GetSurfacePitch","d3d9/IDirect3DCryptoSession9::GetSurfacePitch","mf.idirect3dcryptosession9_getsurfacepitch"]
old-location: mf\idirect3dcryptosession9_getsurfacepitch.htm
tech.root: mf
ms.assetid: 7f9f637e-a693-4fc5-9bf9-a6900aa2ed8c
ms.date: 12/05/2018
ms.keywords: GetSurfacePitch, GetSurfacePitch method [Media Foundation], GetSurfacePitch method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],GetSurfacePitch method, IDirect3DCryptoSession9.GetSurfacePitch, IDirect3DCryptoSession9::GetSurfacePitch, d3d9/IDirect3DCryptoSession9::GetSurfacePitch, mf.idirect3dcryptosession9_getsurfacepitch
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DCryptoSession9::GetSurfacePitch
 - d3d9/IDirect3DCryptoSession9::GetSurfacePitch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.GetSurfacePitch
---

# IDirect3DCryptoSession9::GetSurfacePitch


## -description

Gets the stride of a protected surface.

## -parameters

### -param pSrcSurface

Pointer to the protected surface.

### -param pSurfacePitch

Receives the stride, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A protected surface cannot be locked, so this method provides a way to get the surface stride without locking the surface.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>