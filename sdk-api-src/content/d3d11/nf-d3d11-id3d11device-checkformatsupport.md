---
UID: NF:d3d11.ID3D11Device.CheckFormatSupport
title: ID3D11Device::CheckFormatSupport
author: windows-sdk-content
description: Get the support of a given format on the installed video device.
old-location: direct3d11\id3d11device_checkformatsupport.htm
old-project: direct3d11
ms.assetid: d5442fe8-e510-4bda-9df0-377b465cdd5e
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: 2d26cce0-cf41-b6fc-ed00-e69b3d5ba58f, CheckFormatSupport, CheckFormatSupport method [Direct3D 11], CheckFormatSupport method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CheckFormatSupport method, ID3D11Device.CheckFormatSupport, ID3D11Device::CheckFormatSupport, d3d11/ID3D11Device::CheckFormatSupport, direct3d11.id3d11device_checkformatsupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CheckFormatSupport
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CheckFormatSupport


## -description


Get the support of a given format on the installed video device.


## -parameters




### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> enumeration that describes a format for which to check for support.


### -param pFormatSupport [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A bitfield of <a href="https://msdn.microsoft.com/8c7f62fd-e0fe-4f4d-8c88-ccf1372842f9">D3D11_FORMAT_SUPPORT</a> enumeration values describing how the specified format is supported on the installed device. 
        The values are ORed together.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>Format</i> parameter is <b>NULL</b>, or returns E_FAIL if the 
      described format does not exist.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

