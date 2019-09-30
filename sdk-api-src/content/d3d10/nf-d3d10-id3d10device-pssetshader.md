---
UID: NF:d3d10.ID3D10Device.PSSetShader
title: ID3D10Device::PSSetShader (d3d10.h)
author: windows-sdk-content
description: Sets a pixel shader to the device.
old-location: direct3d10\id3d10device_pssetshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_pssetshader.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],PSSetShader method, ID3D10Device.PSSetShader, ID3D10Device::PSSetShader, PSSetShader, PSSetShader method [Direct3D 10], PSSetShader method [Direct3D 10],ID3D10Device interface, b8f271c1-e769-e3d0-3526-6f08dae50a2a, d3d10/ID3D10Device::PSSetShader, direct3d10.id3d10device_pssetshader
ms.topic: method
f1_keywords: 
 - "d3d10/ID3D10Device.PSSetShader"
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.PSSetShader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::PSSetShader


## -description


Sets a pixel shader to the device.


## -parameters




### -param pPixelShader [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10pixelshader">ID3D10PixelShader</a>*</b>

Pointer to a pixel shader (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10pixelshader">ID3D10PixelShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.


## -returns



Returns nothing.




## -remarks



The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

