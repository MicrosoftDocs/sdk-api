---
UID: NF:d3d11.ID3D11VideoDevice.GetVideoDecoderProfile
title: ID3D11VideoDevice::GetVideoDecoderProfile
author: windows-sdk-content
description: Gets a profile that is supported by the driver.
old-location: mf\id3d11videodevice_getvideodecoderprofile.htm
old-project: medfound
ms.assetid: 8D958469-7FC3-4B4F-82BF-271662CF0088
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetVideoDecoderProfile, GetVideoDecoderProfile method [Media Foundation], GetVideoDecoderProfile method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],GetVideoDecoderProfile method, ID3D11VideoDevice.GetVideoDecoderProfile, ID3D11VideoDevice::GetVideoDecoderProfile, d3d11/ID3D11VideoDevice::GetVideoDecoderProfile, mf.id3d11videodevice_getvideodecoderprofile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDevice.GetVideoDecoderProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoDevice::GetVideoDecoderProfile


## -description


Gets a profile that is supported by the driver.


## -parameters




### -param Index [in]

The zero-based index of the profile. To get the number of profiles that the driver supports, call <a href="https://msdn.microsoft.com/6DCAD69B-3C00-4B3A-97AA-69DF26EF5CD4">ID3D11VideoDevice::GetVideoDecoderProfileCount</a>.


### -param pDecoderProfile [out]

Receives a GUID that identifies the profile.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

