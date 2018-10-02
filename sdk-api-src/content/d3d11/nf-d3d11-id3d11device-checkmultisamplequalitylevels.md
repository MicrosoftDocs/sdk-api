---
UID: NF:d3d11.ID3D11Device.CheckMultisampleQualityLevels
title: ID3D11Device::CheckMultisampleQualityLevels
author: windows-sdk-content
description: Get the number of quality levels available during multisampling.
old-location: direct3d11\id3d11device_checkmultisamplequalitylevels.htm
tech.root: direct3d11
ms.assetid: 346f5dae-3ce2-4c03-ab17-1c46e18efc64
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CheckMultisampleQualityLevels, CheckMultisampleQualityLevels method [Direct3D 11], CheckMultisampleQualityLevels method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CheckMultisampleQualityLevels method, ID3D11Device.CheckMultisampleQualityLevels, ID3D11Device::CheckMultisampleQualityLevels, cc99aa72-2da0-c091-e4b1-047fa6f80bfa, d3d11/ID3D11Device::CheckMultisampleQualityLevels, direct3d11.id3d11device_checkmultisamplequalitylevels
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CheckMultisampleQualityLevels
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::CheckMultisampleQualityLevels


## -description


Get the number of quality levels available during multisampling.


## -parameters




### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The texture format. See <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>.


### -param SampleCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of samples during multisampling.


### -param pNumQualityLevels [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Number of quality levels supported by the adapter. See remarks.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



When multisampling a texture, the number of quality levels available for an adapter is dependent on the texture format used and the number of 
      samples requested. The maximum number of quality levels is defined by D3D11_MAX_MULTISAMPLE_SAMPLE_COUNT in D3D11.h. If this method returns 0, the format 
      and sample count combination is not supported for the installed adapter.

Furthermore, the definition of a quality level is up to each hardware vendor to define, however no facility is provided by Direct3D to help discover 
      this information.

Note that FEATURE_LEVEL_10_1 devices are required to support 4x MSAA for all render targets except R32G32B32A32 and R32G32B32.
      FEATURE_LEVEL_11_0 devices are required to support 4x MSAA for all render target formats, and 8x MSAA for all render target formats 
      except R32G32B32A32 formats.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

