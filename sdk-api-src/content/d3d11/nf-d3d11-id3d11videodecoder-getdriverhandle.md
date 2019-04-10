---
UID: NF:d3d11.ID3D11VideoDecoder.GetDriverHandle
title: ID3D11VideoDecoder::GetDriverHandle (d3d11.h)
author: windows-sdk-content
description: Gets a handle to the driver.
old-location: mf\id3d11videodecoder_getdriverhandle.htm
tech.root: medfound
ms.assetid: CD9A46DB-C16D-4DF4-972B-2CE8398CEE98
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDriverHandle, GetDriverHandle method [Media Foundation], GetDriverHandle method [Media Foundation],ID3D11VideoDecoder interface, ID3D11VideoDecoder interface [Media Foundation],GetDriverHandle method, ID3D11VideoDecoder.GetDriverHandle, ID3D11VideoDecoder::GetDriverHandle, d3d11/ID3D11VideoDecoder::GetDriverHandle, mf.id3d11videodecoder_getdriverhandle
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDecoder.GetDriverHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDecoder::GetDriverHandle


## -description


Gets a handle to the driver.


## -parameters




### -param pDriverHandle [out]

Receives a handle to the driver.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The driver handle can be used to configure content protection.




## -see-also




<a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a>
 

 

