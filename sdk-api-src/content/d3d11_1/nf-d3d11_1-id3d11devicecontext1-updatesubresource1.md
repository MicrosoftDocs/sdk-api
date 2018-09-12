---
UID: NF:d3d11_1.ID3D11DeviceContext1.UpdateSubresource1
title: ID3D11DeviceContext1::UpdateSubresource1
author: windows-sdk-content
description: The CPU copies data from memory to a subresource created in non-mappable memory.
old-location: direct3d11\id3d11devicecontext1_updatesubresource1.htm
tech.root: direct3d11
ms.assetid: 7D89591C-F3F7-4A4F-A91A-AC67D9A573AF
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11DeviceContext1 interface [Direct3D 11],UpdateSubresource1 method, ID3D11DeviceContext1.UpdateSubresource1, ID3D11DeviceContext1::UpdateSubresource1, UpdateSubresource1, UpdateSubresource1 method [Direct3D 11], UpdateSubresource1 method [Direct3D 11],ID3D11DeviceContext1 interface, d3d11_1/ID3D11DeviceContext1::UpdateSubresource1, direct3d11.id3d11devicecontext1_updatesubresource1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11DeviceContext1.UpdateSubresource1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext1::UpdateSubresource1


## -description


The CPU copies data from memory to a subresource created in non-mappable memory.


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a>*</b>

A pointer to the destination resource.


### -param DstSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A zero-based index that identifies the destination subresource. See <a href="https://msdn.microsoft.com/en-us/library/Ff476081(v=VS.85).aspx">D3D11CalcSubresource</a> for more details.


### -param pDstBox [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Ff476089(v=VS.85).aspx">D3D11_BOX</a>*</b>

A pointer to a box that defines the portion of the destination subresource to copy the resource data into. Coordinates are in bytes for buffers and in texels for textures. If <b>NULL</b>, <b>UpdateSubresource1</b> writes the data to the destination subresource with no offset. The dimensions of the source must fit the destination.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>UpdateSubresource1</b> doesn't perform an update operation.


### -param pSrcData [in]

Type: <b>const void*</b>

A pointer to the source data in memory.


### -param SrcRowPitch [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The size of one row of the source data.


### -param SrcDepthPitch [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The size of one depth slice of source data.


### -param CopyFlags [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Hh404451(v=VS.85).aspx">D3D11_COPY_FLAGS</a>-typed value that specifies how to perform the update operation. If you specify zero for no update option, <b>UpdateSubresource1</b> behaves like <a href="https://msdn.microsoft.com/en-us/library/Ff476486(v=VS.85).aspx">ID3D11DeviceContext::UpdateSubresource</a>. For existing display drivers that can't process these flags, the runtime doesn't use them.


## -returns



Returns nothing.




## -remarks



If you call <b>UpdateSubresource1</b> to update a constant buffer, pass any region, and the driver has not been implemented to Windows 8, the runtime drops the call (except <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature level</a> 9.1, 9.2, and 9.3 where the runtime emulates support).  The runtime also drops the call if you update a constant buffer with a partial region whose extent is not aligned to 16-byte granularity (16 bytes being a full constant). When the runtime drops the call, the runtime doesn't call the corresponding device driver interface (DDI).

When you record a call to <a href="https://msdn.microsoft.com/en-us/library/Ff476486(v=VS.85).aspx">UpdateSubresource</a> with an offset <i>pDstBox</i> in a software command list, the offset in <i>pDstBox</i> is incorrectly applied to <i>pSrcData</i> when you play back the command list.  The new-for-Windows 8<b>UpdateSubresource1</b> fixes this issue. In a call to <b>UpdateSubresource1</b>, <i>pDstBox</i> does not affect <i>pSrcData</i>.

For info about various resource types and how <b>UpdateSubresource1</b> might work with each resource type, see <a href="https://msdn.microsoft.com/en-us/library/Ff476900(v=VS.85).aspx">Introduction to a Resource in Direct3D 11</a>. 

<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> If you use <b>UpdateSubresource1</b> or <a href="https://msdn.microsoft.com/en-us/library/Hh404604(v=VS.85).aspx">ID3D11DeviceContext1::CopySubresourceRegion1</a> to copy from a staging resource to a default resource, you can corrupt the destination contents. This occurs if you pass a <b>NULL</b> source box and if the source resource has different dimensions from those of the destination resource or if you use destination offsets, (x, y, and z). In this situation, always pass a source box that is the full size of the source resource.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404598(v=VS.85).aspx">ID3D11DeviceContext1</a>
 

 

