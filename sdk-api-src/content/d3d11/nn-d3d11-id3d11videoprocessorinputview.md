---
UID: NN:d3d11.ID3D11VideoProcessorInputView
title: ID3D11VideoProcessorInputView
author: windows-sdk-content
description: Identifies the input surfaces that can be accessed during video processing.
old-location: mf\id3d11videoprocessorinputview.htm
old-project: medfound
ms.assetid: E76B9CBE-2584-4DBC-8EF4-E9DA105226B9
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ID3D11VideoProcessorInputView, ID3D11VideoProcessorInputView interface [Media Foundation], ID3D11VideoProcessorInputView interface [Media Foundation],described, d3d11/ID3D11VideoProcessorInputView, mf.id3d11videoprocessorinputview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
 - ID3D11VideoProcessorInputView
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11VideoProcessorInputView interface


## -description


Identifies the input surfaces that can be accessed during video processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessorInputView</b> interface inherits from <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>. <b>ID3D11VideoProcessorInputView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11VideoProcessorInputView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FB21A4BA-86BA-4214-B996-A497A8535562">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the properties of the video processor input view.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/3245D2AF-74A1-4068-A0BC-577FD42B353E">ID3D11VideoDevice::CreateVideoProcessorInputView</a>.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>
 

 

