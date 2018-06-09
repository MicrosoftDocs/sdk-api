---
UID: NN:segment.IMSVidEVR
title: IMSVidEVR
author: windows-sdk-content
description: The IMSVidEVR interface represents the Enhanced Video Renderer (EVR) filter within the Video Control filter graph.
old-location: mstv\imsvidevr.htm
old-project: mstv
ms.assetid: 437f515b-0353-4ff2-b8c2-5dd27d4e12f7
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidEVR, IMSVidEVR interface [Microsoft TV Technologies], IMSVidEVR interface [Microsoft TV Technologies],described, IMSVidEVRInterface, mstv.imsvidevr, segment/IMSVidEVR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidEVR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidEVR interface


## -description



The <b>IMSVidEVR</b> interface represents the <a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer</a> (EVR) filter within the Video Control filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidEVR</b> interface inherits from <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a>. <b>IMSVidEVR</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidEVR</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3b5e272-8c71-4e84-b08f-b277eec643c4">get_Presenter</a>
</td>
<td align="left" width="63%">
Retrieves the presenter object for the EVR filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3aaf310-6c42-4013-a3bf-25f9c42cdf81">get_SuppressEffects</a>
</td>
<td align="left" width="63%">
Queries whether the Video Control configures the system for optimal video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/602d92fc-e948-4cea-9bbf-8968c5e31257">put_Presenter</a>
</td>
<td align="left" width="63%">
Sets the presenter object for the EVR filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/399250b6-4f2d-4dbf-b1e8-d32a0673617e">put_SuppressEffects</a>
</td>
<td align="left" width="63%">
Specifies whether the Video Control configures the system for optimal video playback.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidEVR)</code>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

