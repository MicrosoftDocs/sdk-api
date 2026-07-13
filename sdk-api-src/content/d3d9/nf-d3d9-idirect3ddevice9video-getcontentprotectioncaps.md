---
UID: NF:d3d9.IDirect3DDevice9Video.GetContentProtectionCaps
title: IDirect3DDevice9Video::GetContentProtectionCaps (d3d9.h)
description: Queries the display driver for its content protection capabilities.
helpviewer_keywords: ["D3DCRYPTOTYPE_AES128_CTR","D3DCRYPTOTYPE_PROPRIETARY","GetContentProtectionCaps","GetContentProtectionCaps method [Media Foundation]","GetContentProtectionCaps method [Media Foundation]","IDirect3DDevice9Video interface","IDirect3DDevice9Video interface [Media Foundation]","GetContentProtectionCaps method","IDirect3DDevice9Video.GetContentProtectionCaps","IDirect3DDevice9Video::GetContentProtectionCaps","d3d9/IDirect3DDevice9Video::GetContentProtectionCaps","mf.idirect3ddevice9video_getcontentprotectioncaps"]
old-location: mf\idirect3ddevice9video_getcontentprotectioncaps.htm
tech.root: mf
ms.assetid: 4093e64c-340d-4f66-97ed-45bae3b259eb
ms.date: 11/19/2020
ms.keywords: D3DCRYPTOTYPE_AES128_CTR, D3DCRYPTOTYPE_PROPRIETARY, GetContentProtectionCaps, GetContentProtectionCaps method [Media Foundation], GetContentProtectionCaps method [Media Foundation],IDirect3DDevice9Video interface, IDirect3DDevice9Video interface [Media Foundation],GetContentProtectionCaps method, IDirect3DDevice9Video.GetContentProtectionCaps, IDirect3DDevice9Video::GetContentProtectionCaps, d3d9/IDirect3DDevice9Video::GetContentProtectionCaps, mf.idirect3ddevice9video_getcontentprotectioncaps
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
 - IDirect3DDevice9Video::GetContentProtectionCaps
 - d3d9/IDirect3DDevice9Video::GetContentProtectionCaps
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
 - IDirect3DDevice9Video.GetContentProtectionCaps
---

# IDirect3DDevice9Video::GetContentProtectionCaps


## -description

Queries the display driver for its content protection capabilities.

## -parameters

### -param pCryptoType

A pointer to a GUID that specifies the type of encryption to use. The following GUIDs are defined.


**D3DCRYPTOTYPE_AES128_CTR**

128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher.

**D3DCRYPTOTYPE_PROPRIETARY**

Proprietary encryption algorithm.

### -param pDecodeProfile

A pointer to a GUID that specifies the DirectX Video Acceleration 2 (DXVA-2) decoding profile. For a list of possible values, see <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>. If DXVA-2 decoding will not be used, set this parameter to <b>NULL</b>.

### -param pCaps

A pointer to a <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps">D3DCONTENTPROTECTIONCAPS</a> structure. The method fills in this structure with the driver's content protection capabilities.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video">IDirect3DDevice9Video</a>