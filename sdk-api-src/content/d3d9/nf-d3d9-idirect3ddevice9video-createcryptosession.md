---
UID: NF:d3d9.IDirect3DDevice9Video.CreateCryptoSession
title: IDirect3DDevice9Video::CreateCryptoSession (d3d9.h)
author: windows-sdk-content
description: Creates a cryptographic session to encrypt video content that is sent to the display driver.
old-location: mf\idirect3ddevice9video_createcryptosession.htm
tech.root: medfound
ms.assetid: 1c0e3aa4-94d5-4398-a6c0-5466a437162d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateCryptoSession, CreateCryptoSession method [Media Foundation], CreateCryptoSession method [Media Foundation],IDirect3DDevice9Video interface, D3DCRYPTOTYPE_AES128_CTR, D3DCRYPTOTYPE_PROPRIETARY, IDirect3DDevice9Video interface [Media Foundation],CreateCryptoSession method, IDirect3DDevice9Video.CreateCryptoSession, IDirect3DDevice9Video::CreateCryptoSession, d3d9/IDirect3DDevice9Video::CreateCryptoSession, mf.idirect3ddevice9video_createcryptosession
ms.topic: method
f1_keywords: 
 - "d3d9/IDirect3DDevice9Video.CreateCryptoSession"
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
 - IDirect3DDevice9Video.CreateCryptoSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9Video::CreateCryptoSession


## -description


Creates a cryptographic session to encrypt video content that is sent to the display driver.


## -parameters




### -param pCryptoType

Pointer to a GUID that specifies the type of encryption to use. The following GUIDs are defined.



##### )



##### )


### -param pDecodeProfile

Pointer to a GUID that specifies the DirectX Video Acceleration 2 (DXVA-2) decoding profile. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>. If DXVA-2 decoding will not be used, set this parameter to <b>NULL</b>.


### -param ppCryptoSession

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a> interface. The caller must release the interface.


### -param pCryptoHandle

Receives a handle for the session.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video">IDirect3DDevice9Video</a>
 

 

