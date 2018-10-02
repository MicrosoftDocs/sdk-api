---
UID: NF:d3d11_1.ID3D11DeviceContext1.CopySubresourceRegion1
title: ID3D11DeviceContext1::CopySubresourceRegion1
author: windows-sdk-content
description: Copies a region from a source resource to a destination resource.
old-location: direct3d11\id3d11devicecontext1_copysubresourceregion1.htm
tech.root: direct3d11
ms.assetid: 1963011F-C3E2-428D-B667-195A4976510B
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CopySubresourceRegion1, CopySubresourceRegion1 method [Direct3D 11], CopySubresourceRegion1 method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],CopySubresourceRegion1 method, ID3D11DeviceContext1.CopySubresourceRegion1, ID3D11DeviceContext1::CopySubresourceRegion1, d3d11_1/ID3D11DeviceContext1::CopySubresourceRegion1, direct3d11.id3d11devicecontext1_copysubresourceregion1
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
 - ID3D11DeviceContext1.CopySubresourceRegion1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext1::CopySubresourceRegion1


## -description


Copies a region from a source resource to a destination resource.


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a>*</b>

A pointer to the destination resource.


### -param DstSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Destination subresource index.


### -param DstX [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The x-coordinate of the upper-left corner of the destination region.


### -param DstY [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The y-coordinate of the upper-left corner of the destination region. For a 1D subresource, this must be zero.


### -param DstZ [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The z-coordinate of the upper-left corner of the destination region. For a 1D or 2D subresource, this must be zero.


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a>*</b>

A pointer to the source resource.


### -param SrcSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Source subresource index.


### -param pSrcBox [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Ff476089(v=VS.85).aspx">D3D11_BOX</a>*</b>

A pointer to a 3D box that defines the region of the source subresource that <b>CopySubresourceRegion1</b> can copy. If <b>NULL</b>, <b>CopySubresourceRegion1</b> copies the entire source subresource. The box must fit within the source resource.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>CopySubresourceRegion1</b> doesn't perform a copy operation.


### -param CopyFlags [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Hh404451(v=VS.85).aspx">D3D11_COPY_FLAGS</a>-typed value that specifies how to perform the copy operation. If you specify zero for no copy option, <b>CopySubresourceRegion1</b> behaves like <a href="https://msdn.microsoft.com/en-us/library/Ff476394(v=VS.85).aspx">ID3D11DeviceContext::CopySubresourceRegion</a>. For existing display drivers that can't process these flags, the runtime doesn't use them. 


## -returns



Returns nothing




## -remarks



If the display driver supports overlapping, the source and destination subresources can be identical, and the source and destination regions can overlap each other.  For existing display drivers that don’t support overlapping, the runtime drops calls with identical source and destination subresources, regardless of whether the regions overlap.  To determine whether the display driver supports overlapping, check the <b>CopyWithOverlap</b> member of <a href="https://msdn.microsoft.com/en-us/library/Hh404457(v=VS.85).aspx">D3D11_FEATURE_DATA_D3D11_OPTIONS</a>. This overlapping support enables additional scroll functionality in a call to <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a>.

<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> If you use <a href="https://msdn.microsoft.com/en-us/library/Hh446790(v=VS.85).aspx">ID3D11DeviceContext1::UpdateSubresource1</a> or <b>CopySubresourceRegion1</b> to copy from a staging resource to a default resource, you can corrupt the destination contents. This occurs if you pass a <b>NULL</b> source box and if the source resource has different dimensions from those of the destination resource or if you use destination offsets, (x, y, and z). In this situation, always pass a source box that is the full size of the source resource.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404598(v=VS.85).aspx">ID3D11DeviceContext1</a>
 

 

