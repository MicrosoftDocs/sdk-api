---
UID: NN:d3d11.ID3D11VideoProcessorEnumerator
title: ID3D11VideoProcessorEnumerator
author: windows-sdk-content
description: Enumerates the video processor capabilities of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videoprocessorenumerator.htm
old-project: medfound
ms.assetid: 8713B4C6-B08E-4616-92A7-05280CCE7AB3
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ID3D11VideoProcessorEnumerator, ID3D11VideoProcessorEnumerator interface [Media Foundation], ID3D11VideoProcessorEnumerator interface [Media Foundation],described, d3d11/ID3D11VideoProcessorEnumerator, mf.id3d11videoprocessorenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoProcessorEnumerator
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11VideoProcessorEnumerator interface


## -description


Enumerates the video processor capabilities of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessorEnumerator</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11VideoProcessorEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoProcessorEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451616">CheckVideoProcessorFormat</a>
</td>
<td align="left" width="63%">
Queries whether the video processor supports a specified video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451674">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BDB52B2E-1D76-4867-AD58-2A77BC5B6ABD">GetVideoProcessorContentDesc</a>
</td>
<td align="left" width="63%">
Gets the content description that was used to create this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451676">GetVideoProcessorCustomRate</a>
</td>
<td align="left" width="63%">
Gets a list of custom frame rates that a video processor supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451689">GetVideoProcessorFilterRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for an image filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451690">GetVideoProcessorRateConversionCaps</a>
</td>
<td align="left" width="63%">
Returns a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/992C699D-A499-494E-AEDF-A6688CB14D70">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>.

To create an instance of the video processor, pass the <b>ID3D11VideoProcessorEnumerator</b> pointer to the <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/BBC4C5BC-2DA0-48BD-B182-FBF62A2491A7">ID3D11VideoProcessorEnumerator</a>
 

 

