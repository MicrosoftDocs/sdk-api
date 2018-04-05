---
UID: NF:dxva.IDirect3DVideoDevice9.CreateSurface
title: IDirect3DVideoDevice9::CreateSurface method
author: windows-driver-content
description: Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.
old-location: mf\idirect3dvideodevice9_createsurface.htm
old-project: medfound
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: CreateSurface method [Media Foundation], CreateSurface method [Media Foundation], IDirect3DVideoDevice9 interface, CreateSurface,IDirect3DVideoDevice9.CreateSurface, IDirect3DVideoDevice9, IDirect3DVideoDevice9 interface [Media Foundation], CreateSurface method, IDirect3DVideoDevice9::CreateSurface, dxva/IDirect3DVideoDevice9::CreateSurface, mf.idirect3dvideodevice9_createsurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COPP_TVProtectionStandard
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva.h
api_name:
-	IDirect3DVideoDevice9.CreateSurface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DVideoDevice9::CreateSurface method


## -description


Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.

To get the surface requirements, call <a href="https://msdn.microsoft.com/5a9fb077-fd79-4faa-a0f8-b3ac987adf36">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo</a> and examine the returned <a href="https://msdn.microsoft.com/dabef388-d883-48a6-9abc-218dc163ef63">DXVACompBufferInfo</a> structures.


## -parameters




### -param Width

The width of the surface, in pixels. Set this parameter equal to <b>DXVACompBufferInfo.WidthToCreate</b>.


### -param Height

The height of the surface, in pixels. Set this parameter equal to <b>DXVACompBufferInfo.HeightToCreate</b>.


### -param BackBuffers

The number of back buffers. This parameter can be zero.


### -param Format

The pixel format, specified as a <b>D3DFORMAT</b> value. Set this parameter equal to <b>DXVACompBufferInfo.Format</b>.


### -param Pool

The memory pool in which to create the surface, specified as a <b>D3DPOOL</b> value. Set this parameter equal to <b>DXVACompBufferInfo.Pool</b>.


### -param Usage

A bitwise <b>OR</b> of one or more <b>D3DUSAGE</b> constants. Set this parameter equal to <b>DXVACompBufferInfo.Usage</b>.


### -param ppSurface

Receives a pointer to the <b>IDirect3DSurface9</b> interface. The caller must release the interface.


### -param pSharedHandle

Reserved. Set to <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/abe3beac-f3f8-413d-8b83-9da3340b19ac">IDirect3DVideoDevice9</a>
 

 

