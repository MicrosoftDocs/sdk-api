---
UID: NF:d3d11_2.ID3D11Device2.CheckMultisampleQualityLevels1
title: ID3D11Device2::CheckMultisampleQualityLevels1
author: windows-sdk-content
description: Get the number of quality levels available during multisampling.
old-location: direct3d11\id3d11device2_checkmultisamplequalitylevels1.htm
old-project: direct3d11
ms.assetid: 1248F56D-C9A3-415E-85BB-E4FFC8283497
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: CheckMultisampleQualityLevels1, CheckMultisampleQualityLevels1 method [Direct3D 11], CheckMultisampleQualityLevels1 method [Direct3D 11],ID3D11Device2 interface, ID3D11Device2 interface [Direct3D 11],CheckMultisampleQualityLevels1 method, ID3D11Device2.CheckMultisampleQualityLevels1, ID3D11Device2::CheckMultisampleQualityLevels1, d3d11_2/ID3D11Device2::CheckMultisampleQualityLevels1, direct3d11.id3d11device2_checkmultisamplequalitylevels1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_TILE_RANGE_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Device2.CheckMultisampleQualityLevels1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device2::CheckMultisampleQualityLevels1


## -description


Get the number of quality levels available during multisampling.


## -parameters




### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The texture format during multisampling. 


### -param SampleCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of samples during multisampling.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/756AD5B2-3B6A-4F28-B034-93F59C41D02B">D3D11_CHECK_MULTISAMPLE_QUALITY_LEVELS_FLAGS</a> values that are combined by using a bitwise OR operation. Currently, only <a href="d3d11_check_multisample_quality_levels_flags.htm">D3D11_CHECK_MULTISAMPLE_QUALITY_LEVELS_TILED_RESOURCE</a> is supported. 


### -param pNumQualityLevels [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable the receives the number of quality levels supported by the adapter. See Remarks.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



When you multisample a texture, the number of quality levels available for an adapter is dependent on the texture format that you use and the number of 
      samples that you request. The maximum number of quality levels is defined by <b>D3D11_MAX_MULTISAMPLE_SAMPLE_COUNT</b> in D3D11.h. If this method returns 0, the format 
      and sample count combination is not supported for the installed adapter.

Furthermore, the definition of a quality level is up to each hardware vendor to define, however no facility is provided by Direct3D to help discover 
      this information.

Note that FEATURE_LEVEL_10_1 devices are required to support 4x MSAA for all render targets except R32G32B32A32 and R32G32B32.
      FEATURE_LEVEL_11_0 devices are required to support 4x MSAA for all render target formats, and 8x MSAA for all render target formats 
      except R32G32B32A32 formats.




## -see-also




<a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>
 

 

