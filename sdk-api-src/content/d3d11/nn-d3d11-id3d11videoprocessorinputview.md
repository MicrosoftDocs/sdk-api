---
UID: NN:d3d11.ID3D11VideoProcessorInputView
title: ID3D11VideoProcessorInputView
author: windows-sdk-content
description: Identifies the input surfaces that can be accessed during video processing.
old-location: mf\id3d11videoprocessorinputview.htm
tech.root: MedFound
ms.assetid: E76B9CBE-2584-4DBC-8EF4-E9DA105226B9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ID3D11VideoProcessorInputView, ID3D11VideoProcessorInputView interface [Media Foundation], ID3D11VideoProcessorInputView interface [Media Foundation],described, d3d11/ID3D11VideoProcessorInputView, mf.id3d11videoprocessorinputview
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
 - ID3D11VideoProcessorInputView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoProcessorInputView interface


## -description


Identifies the input surfaces that can be accessed during video processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11VideoProcessorInputView</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a>. <b>ID3D11VideoProcessorInputView</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh447808(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the properties of the video processor input view.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/en-us/library/Hh447790(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessorInputView</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447679(v=VS.85).aspx">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a>
 

 

