---
UID: NF:d3d10.ID3D10Device.CheckMultisampleQualityLevels
title: ID3D10Device::CheckMultisampleQualityLevels
author: windows-sdk-content
description: Get the number of quality levels available during multisampling.
old-location: direct3d10\id3d10device_checkmultisamplequalitylevels.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_checkmultisamplequalitylevels.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 5555dfc7-c61e-e6e9-a6a5-956255410a73, CheckMultisampleQualityLevels, CheckMultisampleQualityLevels method [Direct3D 10], CheckMultisampleQualityLevels method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CheckMultisampleQualityLevels method, ID3D10Device.CheckMultisampleQualityLevels, ID3D10Device::CheckMultisampleQualityLevels, d3d10/ID3D10Device::CheckMultisampleQualityLevels, direct3d10.id3d10device_checkmultisamplequalitylevels
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D10Device.CheckMultisampleQualityLevels
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.CheckMultisampleQualityLevels
: 
---

# ID3D10Device::CheckMultisampleQualityLevels


## -description


Get the number of quality levels available during multisampling.


## -parameters




### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

The texture format. See <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>.


### -param SampleCount [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of samples during multisampling.


### -param pNumQualityLevels [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a>*</b>

Number of quality levels supported by the adapter. See remarks.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



When multisampling a texture, the number of quality levels available for an adapter is dependent on the texture format used and the number of samples
      requested. The maximum sample count defined by D3D10_MAX_MULTISAMPLE_SAMPLE_COUNT in d3d10.h is 32. If the returned value of
      <i>pNumQualityLevels</i> is 0, the format and sample count combination is not supported for the installed adapter.

Furthermore, the definition of a quality level is up to each hardware vendor to define, however no facility is provided by Direct3D to help discover 
      this information.

Direct3D 10.1 devices are required to support 4x MSAA for all formats except R32G32B32A32 and R32G32B32 formats.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

