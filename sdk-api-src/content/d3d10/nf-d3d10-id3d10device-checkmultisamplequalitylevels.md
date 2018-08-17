---
UID: NF:d3d10.ID3D10Device.CheckMultisampleQualityLevels
title: ID3D10Device::CheckMultisampleQualityLevels
author: windows-sdk-content
description: Get the number of quality levels available during multisampling.
old-location: direct3d10\id3d10device_checkmultisamplequalitylevels.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_checkmultisamplequalitylevels.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 5555dfc7-c61e-e6e9-a6a5-956255410a73, CheckMultisampleQualityLevels, CheckMultisampleQualityLevels method [Direct3D 10], CheckMultisampleQualityLevels method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CheckMultisampleQualityLevels method, ID3D10Device.CheckMultisampleQualityLevels, ID3D10Device::CheckMultisampleQualityLevels, d3d10/ID3D10Device::CheckMultisampleQualityLevels, direct3d10.id3d10device_checkmultisamplequalitylevels
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CheckMultisampleQualityLevels
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CheckMultisampleQualityLevels


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

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



When multisampling a texture, the number of quality levels available for an adapter is dependent on the texture format used and the number of samples
      requested. The maximum sample count defined by D3D10_MAX_MULTISAMPLE_SAMPLE_COUNT in d3d10.h is 32. If the returned value of
      <i>pNumQualityLevels</i> is 0, the format and sample count combination is not supported for the installed adapter.

Furthermore, the definition of a quality level is up to each hardware vendor to define, however no facility is provided by Direct3D to help discover 
      this information.

Direct3D 10.1 devices are required to support 4x MSAA for all formats except R32G32B32A32 and R32G32B32 formats.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

