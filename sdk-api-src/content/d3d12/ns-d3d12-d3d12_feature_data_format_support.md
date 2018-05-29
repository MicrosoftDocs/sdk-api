---
UID: NS:d3d12.D3D12_FEATURE_DATA_FORMAT_SUPPORT
title: D3D12_FEATURE_DATA_FORMAT_SUPPORT
author: windows-sdk-content
description: Describes which resources are supported by the current graphics driver for a given format.
old-location: direct3d12\d3d12_feature_data_format_support.htm
old-project: direct3d12
ms.assetid: 6E4EB08F-0B60-4B1E-AD27-8F0AE2BD0766
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_FEATURE_DATA_FORMAT_SUPPORT, D3D12_FEATURE_DATA_FORMAT_SUPPORT structure, d3d12/D3D12_FEATURE_DATA_FORMAT_SUPPORT, direct3d12.d3d12_feature_data_format_support
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
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
req.typenames: D3D12_FEATURE_DATA_FORMAT_SUPPORT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_FEATURE_DATA_FORMAT_SUPPORT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_FEATURE_DATA_FORMAT_SUPPORT structure


## -description



          Describes which resources are supported by the current graphics driver for a given format.
        


## -struct-fields




### -field Format


            A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value for the format to return info about.
          


### -field Support1


            A combination of <a href="https://msdn.microsoft.com/D987B228-4BC9-4A07-96A0-A518F8F52B06">D3D12_FORMAT_SUPPORT1</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies which resources are supported.
          


### -field Support2


            A combination of <a href="https://msdn.microsoft.com/29B53FBE-2FF3-4A3A-8392-30781541C396">D3D12_FORMAT_SUPPORT2</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies which unordered resource options are supported.
          


## -remarks




        Refer to the enum <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>.
      

<h3><a id="Hardware_support_for_DXGI_Formats"></a><a id="hardware_support_for_dxgi_formats"></a><a id="HARDWARE_SUPPORT_FOR_DXGI_FORMATS"></a>Hardware support for DXGI Formats</h3>
To view tables of DXGI formats and hardware features, refer to:

<ul>
<li>
<a href="https://msdn.microsoft.com/0DC50FF3-3193-4F3B-9976-EE504C6FCC87">DXGI Format  Support for Direct3D Feature Level 12.1 Hardware</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A039A82B-2E30-41A6-96B5-AD5538FE2285">DXGI Format  Support for Direct3D Feature Level 12.0 Hardware</a>
</li>
<li>
<a href="https://msdn.microsoft.com/90EADE0C-A984-4993-A3F8-D045C535DE64">DXGI Format  Support for Direct3D Feature Level 11.1 Hardware</a>
</li>
<li>
<a href="https://msdn.microsoft.com/735CDA40-557F-4D47-87B7-97A8E120B9D2">DXGI Format  Support for Direct3D Feature Level 11.0 Hardware</a>
</li>
<li>
<a href="direct3ddxgi.d3d11_graphics_programming_guide_dxgi_hw_formats_10level9">Hardware Support for Direct3D 10Level9 Formats</a>
</li>
<li>
<a href="https://msdn.microsoft.com/011ad888-1c1d-4cbd-ab70-12fb8adc000f">Hardware Support for Direct3D 10.1 Formats</a>
</li>
<li>
<a href="https://msdn.microsoft.com/529ced9a-d4fa-4b41-932b-343638cd5c7c">Hardware Support for Direct3D 10 Formats</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>
 

 

