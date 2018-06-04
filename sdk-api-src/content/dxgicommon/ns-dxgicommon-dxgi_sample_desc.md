---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DXGI_SAMPLE_DESC structure


## -description


Describes multi-sampling parameters for a resource.


## -struct-fields




### -field Count

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of multisamples per pixel.


### -field Quality

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The image quality level. The higher the quality, the lower the performance. The valid range is between zero and one less than the level returned 
        by <a href="https://msdn.microsoft.com/5b43c582-3ddb-49d8-be0d-1a784f482750">ID3D10Device::CheckMultisampleQualityLevels</a> for Direct3D 10 or <a href="https://msdn.microsoft.com/346f5dae-3ce2-4c03-ab17-1c46e18efc64">ID3D11Device::CheckMultisampleQualityLevels</a> for Direct3D 11.

For Direct3D 10.1 and Direct3D 11, you can use two special quality level values. For more information about these quality level values, see Remarks.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure.

The default sampler mode, with no anti-aliasing, has a count of 1 and a quality level of 0.

If multi-sample antialiasing is being used, all bound render targets and depth buffers must have the same sample counts and quality levels.

<table>
<tr>
<td>
Differences between Direct3D 10.0 and Direct3D 10.1 and between Direct3D 10.0 and Direct3D 11:

Direct3D 10.1 has defined two standard quality levels:  
            <b>D3D10_STANDARD_MULTISAMPLE_PATTERN</b> and <b>D3D10_CENTER_MULTISAMPLE_PATTERN</b> in the <b>D3D10_STANDARD_MULTISAMPLE_QUALITY_LEVELS</b> enumeration in D3D10_1.h.

Direct3D 11 has defined two standard quality levels:  
            <b>D3D11_STANDARD_MULTISAMPLE_PATTERN</b> and <b>D3D11_CENTER_MULTISAMPLE_PATTERN</b> in the <a href="https://msdn.microsoft.com/20c558ae-e9c3-4bab-8c11-264d626f2cff">D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS</a> enumeration in D3D11.h.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

