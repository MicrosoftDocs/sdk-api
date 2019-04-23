---
UID: NS:d3d12.D3D12_FEATURE_DATA_FORMAT_SUPPORT
title: D3D12_FEATURE_DATA_FORMAT_SUPPORT (d3d12.h)
author: windows-sdk-content
description: Describes which resources are supported by the current graphics driver for a given format.
old-location: direct3d12\d3d12_feature_data_format_support.htm
tech.root: direct3d12
ms.assetid: 6E4EB08F-0B60-4B1E-AD27-8F0AE2BD0766
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_FORMAT_SUPPORT, D3D12_FEATURE_DATA_FORMAT_SUPPORT structure, d3d12/D3D12_FEATURE_DATA_FORMAT_SUPPORT, direct3d12.d3d12_feature_data_format_support
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_FEATURE_DATA_FORMAT_SUPPORT
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE_DATA_FORMAT_SUPPORT
req.redist: 
ms.custom: 19H1
---

# D3D12_FEATURE_DATA_FORMAT_SUPPORT structure


## -description


Describes which resources are supported by the current graphics driver for a given format.


## -struct-fields




### -field Format

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value for the format to return info about.


### -field Support1

A combination of <a href="https://msdn.microsoft.com/D987B228-4BC9-4A07-96A0-A518F8F52B06">D3D12_FORMAT_SUPPORT1</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies which resources are supported.


### -field Support2

A combination of <a href="https://msdn.microsoft.com/29B53FBE-2FF3-4A3A-8392-30781541C396">D3D12_FORMAT_SUPPORT2</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies which unordered resource options are supported.


## -remarks



Refer to <a href="https://msdn.microsoft.com/en-us/library/Dn914603(v=VS.85).aspx">Typed unordered access view loads</a> for an example use of this structure.

Also see <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>.

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
<a href="https://msdn.microsoft.com/library/Ff471324(v=VS.85).aspx">Hardware Support for Direct3D 10Level9 Formats</a>
</li>
<li>
<a href="https://docs.microsoft.com/en-us/windows/desktop/direct3ddxgi/format-support-for-direct3d-feature-level-10-1-hardware">Hardware Support for Direct3D 10.1 Formats</a>
</li>
<li>
<a href="https://docs.microsoft.com/en-us/windows/desktop/direct3ddxgi/format-support-for-direct3d-feature-level-10-0-hardware">Hardware Support for Direct3D 10 Formats</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn914603(v=VS.85).aspx">Typed unordered access view loads</a>
 

 

