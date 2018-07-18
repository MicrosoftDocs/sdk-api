---
UID: NN:d3d11_1.ID3D11VideoProcessorEnumerator1
title: ID3D11VideoProcessorEnumerator1
author: windows-sdk-content
description: Enumerates the video processor capabilities of a Microsoft Direct3D 11 device.
old-location: mf\id3d11videoprocessorenumerator1.htm
old-project: medfound
ms.assetid: BBC4C5BC-2DA0-48BD-B182-FBF62A2491A7
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ID3D11VideoProcessorEnumerator1, ID3D11VideoProcessorEnumerator1 interface [Media Foundation], ID3D11VideoProcessorEnumerator1 interface [Media Foundation],described, d3d11_1/ID3D11VideoProcessorEnumerator1, mf.id3d11videoprocessorenumerator1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoProcessorEnumerator1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11VideoProcessorEnumerator1 interface


## -description


Enumerates the video processor capabilities of a Microsoft Direct3D 11 device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessorEnumerator1</b> interface inherits from <a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a>. <b>ID3D11VideoProcessorEnumerator1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoProcessorEnumerator1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn906317">CheckVideoProcessorFormatConversion</a>
</td>
<td align="left" width="63%">
Indicates whether the driver supports the specified combination of format and colorspace conversions.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/992C699D-A499-494E-AEDF-A6688CB14D70">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>. 




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a>
 

 

