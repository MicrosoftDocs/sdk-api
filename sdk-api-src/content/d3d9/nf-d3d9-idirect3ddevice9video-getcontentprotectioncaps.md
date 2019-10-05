---
UID: NF:d3d9.IDirect3DDevice9Video.GetContentProtectionCaps
title: IDirect3DDevice9Video::GetContentProtectionCaps (d3d9.h)
author: windows-sdk-content
description: Queries the display driver for its content protection capabilities.
old-location: mf\idirect3ddevice9video_getcontentprotectioncaps.htm
tech.root: medfound
ms.assetid: 4093e64c-340d-4f66-97ed-45bae3b259eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3DCRYPTOTYPE_AES128_CTR, D3DCRYPTOTYPE_PROPRIETARY, GetContentProtectionCaps, GetContentProtectionCaps method [Media Foundation], GetContentProtectionCaps method [Media Foundation],IDirect3DDevice9Video interface, IDirect3DDevice9Video interface [Media Foundation],GetContentProtectionCaps method, IDirect3DDevice9Video.GetContentProtectionCaps, IDirect3DDevice9Video::GetContentProtectionCaps, d3d9/IDirect3DDevice9Video::GetContentProtectionCaps, mf.idirect3ddevice9video_getcontentprotectioncaps
ms.topic: method
f1_keywords:
- d3d9/IDirect3DDevice9Video.GetContentProtectionCaps
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d9.h
api_name:
- IDirect3DDevice9Video.GetContentProtectionCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9Video::GetContentProtectionCaps


## -description


Queries the display driver for its content protection capabilities.


## -parameters




### -param pCryptoType

A pointer to a GUID that specifies the type of encryption to use. The following GUIDs are defined.



##### )



##### )


### -param pDecodeProfile

A pointer to a GUID that specifies the DirectX Video Acceleration 2 (DXVA-2) decoding profile. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>. If DXVA-2 decoding will not be used, set this parameter to <b>NULL</b>.


### -param pCaps

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps">D3DCONTENTPROTECTIONCAPS</a> structure. The method fills in this structure with the driver's content protection capabilities.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video">IDirect3DDevice9Video</a>
 

 

