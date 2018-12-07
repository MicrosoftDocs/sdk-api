---
UID: NN:d3d11.ID3D11VideoProcessorEnumerator
title: ID3D11VideoProcessorEnumerator
author: windows-sdk-content
description: Enumerates the video processor capabilities of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videoprocessorenumerator.htm
tech.root: medfound
ms.assetid: 8713B4C6-B08E-4616-92A7-05280CCE7AB3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoProcessorEnumerator, ID3D11VideoProcessorEnumerator interface [Media Foundation], ID3D11VideoProcessorEnumerator interface [Media Foundation],described, d3d11/ID3D11VideoProcessorEnumerator, mf.id3d11videoprocessorenumerator
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# ID3D11VideoProcessorEnumerator interface


## -description


Enumerates the video processor capabilities of a Microsoft Direct3D 11 device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessorEnumerator</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11VideoProcessorEnumerator</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh447801(v=VS.85).aspx">CheckVideoProcessorFormat</a>
</td>
<td align="left" width="63%">
Queries whether the video processor supports a specified video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447803(v=VS.85).aspx">GetVideoProcessorContentDesc</a>
</td>
<td align="left" width="63%">
Gets the content description that was used to create this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447804(v=VS.85).aspx">GetVideoProcessorCustomRate</a>
</td>
<td align="left" width="63%">
Gets a list of custom frame rates that a video processor supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447805(v=VS.85).aspx">GetVideoProcessorFilterRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for an image filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh447806(v=VS.85).aspx">GetVideoProcessorRateConversionCaps</a>
</td>
<td align="left" width="63%">
Returns a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/Hh447789(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>.

To create an instance of the video processor, pass the <b>ID3D11VideoProcessorEnumerator</b> pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn894146(v=VS.85).aspx">ID3D11VideoProcessorEnumerator</a>
 

 

