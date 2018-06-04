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

# ID3D11DeviceContext1::UpdateSubresource1


## -description


The CPU copies data from memory to a subresource created in non-mappable memory.


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the destination resource.


### -param DstSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index that identifies the destination subresource. See <a href="https://msdn.microsoft.com/643a21f7-3c2e-4d62-9236-051f51d31241">D3D11CalcSubresource</a> for more details.


### -param pDstBox [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0cc98805-a36e-41aa-a24f-51fbcf5070df">D3D11_BOX</a>*</b>

A pointer to a box that defines the portion of the destination subresource to copy the resource data into. Coordinates are in bytes for buffers and in texels for textures. If <b>NULL</b>, <b>UpdateSubresource1</b> writes the data to the destination subresource with no offset. The dimensions of the source must fit the destination.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>UpdateSubresource1</b> doesn't perform an update operation.


### -param pSrcData [in]

Type: <b>const void*</b>

A pointer to the source data in memory.


### -param SrcRowPitch [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of one row of the source data.


### -param SrcDepthPitch [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of one depth slice of source data.


### -param CopyFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A <a href="https://msdn.microsoft.com/2141A053-931B-42F2-BC8C-AAE9F4739ED7">D3D11_COPY_FLAGS</a>-typed value that specifies how to perform the update operation. If you specify zero for no update option, <b>UpdateSubresource1</b> behaves like <a href="https://msdn.microsoft.com/2d8ef5a2-204a-434d-918a-104419050233">ID3D11DeviceContext::UpdateSubresource</a>. For existing display drivers that can't process these flags, the runtime doesn't use them.


## -returns



Returns nothing.




## -remarks



If you call <b>UpdateSubresource1</b> to update a constant buffer, pass any region, and the driver has not been implemented to Windows 8, the runtime drops the call (except <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> 9.1, 9.2, and 9.3 where the runtime emulates support).  The runtime also drops the call if you update a constant buffer with a partial region whose extent is not aligned to 16-byte granularity (16 bytes being a full constant). When the runtime drops the call, the runtime doesn't call the corresponding device driver interface (DDI).

When you record a call to <a href="https://msdn.microsoft.com/2d8ef5a2-204a-434d-918a-104419050233">UpdateSubresource</a> with an offset <i>pDstBox</i> in a software command list, the offset in <i>pDstBox</i> is incorrectly applied to <i>pSrcData</i> when you play back the command list.  The new-for-Windows 8<b>UpdateSubresource1</b> fixes this issue. In a call to <b>UpdateSubresource1</b>, <i>pDstBox</i> does not affect <i>pSrcData</i>.

For info about various resource types and how <b>UpdateSubresource1</b> might work with each resource type, see <a href="https://msdn.microsoft.com/9e991ab0-9648-484a-9a2c-5391ee5abf20">Introduction to a Resource in Direct3D 11</a>. 

<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> If you use <b>UpdateSubresource1</b> or <a href="https://msdn.microsoft.com/1963011F-C3E2-428D-B667-195A4976510B">ID3D11DeviceContext1::CopySubresourceRegion1</a> to copy from a staging resource to a default resource, you can corrupt the destination contents. This occurs if you pass a <b>NULL</b> source box and if the source resource has different dimensions from those of the destination resource or if you use destination offsets, (x, y, and z). In this situation, always pass a source box that is the full size of the source resource.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>
 

 

