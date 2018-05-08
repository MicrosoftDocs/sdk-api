---
UID: NF:d3d12.ID3D12Device.CheckFeatureSupport
title: ID3D12Device::CheckFeatureSupport
author: windows-driver-content
description: Gets information about the features that are supported by the current graphics driver.
old-location: direct3d12\id3d12device_checkfeaturesupport.htm
old-project: direct3d12
ms.assetid: 2E986E37-30C7-45FE-BC8B-A6DD5670938F
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: CheckFeatureSupport, CheckFeatureSupport method, CheckFeatureSupport method,ID3D12Device interface, ID3D12Device interface,CheckFeatureSupport method, ID3D12Device.CheckFeatureSupport, ID3D12Device::CheckFeatureSupport, d3d12/ID3D12Device::CheckFeatureSupport, direct3d12.id3d12device_checkfeaturesupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D12.dll
api_name:
-	ID3D12Device.CheckFeatureSupport
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CheckFeatureSupport


## -description



          Gets information about the features that are supported by the current graphics driver.


## -parameters




### -param Feature

Type: <b><a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a></b>


              A <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>-typed value that describes the feature to query for support.
            


### -param pFeatureSupportData [in, out]

Type: <b>void*</b>


              The passed structure is filled with data that describes the feature support.
              To see the structure types, see the Remarks section in <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE enumeration</a>.
            


	      When calling CheckFeatureSupport, the <b>HighestShaderModel</b> field of the structure passed in <i>pFeatureSupportData</i> should be initialized to the highest shader model that the application understands. After the function returns successfully, the <b>HighestShaderModel</b> field will contain the highest shader model that's supported by the device and is no higher than the shader model passed in.
	    


### -param FeatureSupportDataSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


              The size of the structure passed to the <i>pFeatureSupportData</i> parameter.
            


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


              Returns <b>S_OK</b> if successful; otherwise, returns <b>E_INVALIDARG</b> if an unsupported data type is passed to the <i>pFeatureSupportData</i> parameter or a size mismatch is detected for the <i>FeatureSupportDataSize</i> parameter.
            




## -remarks



Refer to <a href="https://msdn.microsoft.com/ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8">Capability Querying</a>.

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

#### Examples


          The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D1211on12</a> sample uses <b>ID3D12Device::CheckFeatureSupport</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>inline UINT8 D3D12GetFormatPlaneCount(
    _In_ ID3D12Device* pDevice,
    DXGI_FORMAT Format
    )
{
    D3D12_FEATURE_DATA_FORMAT_INFO formatInfo = {Format};
    if (FAILED(pDevice-&gt;CheckFeatureSupport(D3D12_FEATURE_FORMAT_INFO, &amp;formatInfo, sizeof(formatInfo))))
    {
        return 0;
    }
    return formatInfo.PlaneCount;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

