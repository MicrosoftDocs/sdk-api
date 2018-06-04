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

# ID3D11DeviceContext1::CopySubresourceRegion1


## -description


Copies a region from a source resource to a destination resource.


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the destination resource.


### -param DstSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Destination subresource index.


### -param DstX [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The x-coordinate of the upper-left corner of the destination region.


### -param DstY [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The y-coordinate of the upper-left corner of the destination region. For a 1D subresource, this must be zero.


### -param DstZ [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The z-coordinate of the upper-left corner of the destination region. For a 1D or 2D subresource, this must be zero.


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the source resource.


### -param SrcSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Source subresource index.


### -param pSrcBox [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0cc98805-a36e-41aa-a24f-51fbcf5070df">D3D11_BOX</a>*</b>

A pointer to a 3D box that defines the region of the source subresource that <b>CopySubresourceRegion1</b> can copy. If <b>NULL</b>, <b>CopySubresourceRegion1</b> copies the entire source subresource. The box must fit within the source resource.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>CopySubresourceRegion1</b> doesn't perform a copy operation.


### -param CopyFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A <a href="https://msdn.microsoft.com/2141A053-931B-42F2-BC8C-AAE9F4739ED7">D3D11_COPY_FLAGS</a>-typed value that specifies how to perform the copy operation. If you specify zero for no copy option, <b>CopySubresourceRegion1</b> behaves like <a href="https://msdn.microsoft.com/aed89483-9870-445d-96e3-a9cee764f0ad">ID3D11DeviceContext::CopySubresourceRegion</a>. For existing display drivers that can't process these flags, the runtime doesn't use them. 


## -returns



Returns nothing




## -remarks



If the display driver supports overlapping, the source and destination subresources can be identical, and the source and destination regions can overlap each other.  For existing display drivers that don’t support overlapping, the runtime drops calls with identical source and destination subresources, regardless of whether the regions overlap.  To determine whether the display driver supports overlapping, check the <b>CopyWithOverlap</b> member of <a href="https://msdn.microsoft.com/02A3B423-75AB-4F44-BEBE-B8039EF384DC">D3D11_FEATURE_DATA_D3D11_OPTIONS</a>. This overlapping support enables additional scroll functionality in a call to <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a>.

<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> If you use <a href="https://msdn.microsoft.com/7D89591C-F3F7-4A4F-A91A-AC67D9A573AF">ID3D11DeviceContext1::UpdateSubresource1</a> or <b>CopySubresourceRegion1</b> to copy from a staging resource to a default resource, you can corrupt the destination contents. This occurs if you pass a <b>NULL</b> source box and if the source resource has different dimensions from those of the destination resource or if you use destination offsets, (x, y, and z). In this situation, always pass a source box that is the full size of the source resource.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>
 

 

