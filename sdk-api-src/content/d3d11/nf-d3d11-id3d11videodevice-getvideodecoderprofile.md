---
UID: NF:d3d11.ID3D11VideoDevice.GetVideoDecoderProfile
title: ID3D11VideoDevice::GetVideoDecoderProfile (d3d11.h)
description: Gets a profile that is supported by the driver.
helpviewer_keywords: ["GetVideoDecoderProfile","GetVideoDecoderProfile method [Media Foundation]","GetVideoDecoderProfile method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","GetVideoDecoderProfile method","ID3D11VideoDevice.GetVideoDecoderProfile","ID3D11VideoDevice::GetVideoDecoderProfile","d3d11/ID3D11VideoDevice::GetVideoDecoderProfile","mf.id3d11videodevice_getvideodecoderprofile"]
old-location: mf\id3d11videodevice_getvideodecoderprofile.htm
tech.root: mf
ms.assetid: 8D958469-7FC3-4B4F-82BF-271662CF0088
ms.date: 12/05/2018
ms.keywords: GetVideoDecoderProfile, GetVideoDecoderProfile method [Media Foundation], GetVideoDecoderProfile method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],GetVideoDecoderProfile method, ID3D11VideoDevice.GetVideoDecoderProfile, ID3D11VideoDevice::GetVideoDecoderProfile, d3d11/ID3D11VideoDevice::GetVideoDecoderProfile, mf.id3d11videodevice_getvideodecoderprofile
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ID3D11VideoDevice::GetVideoDecoderProfile
 - d3d11/ID3D11VideoDevice::GetVideoDecoderProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDevice.GetVideoDecoderProfile
---

# ID3D11VideoDevice::GetVideoDecoderProfile


## -description

Gets a profile that is supported by the driver.

## -parameters

### -param Index [in]

The zero-based index of the profile. To get the number of profiles that the driver supports, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount">ID3D11VideoDevice::GetVideoDecoderProfileCount</a>.

### -param pDecoderProfile [out]

Receives a GUID that identifies the profile.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>