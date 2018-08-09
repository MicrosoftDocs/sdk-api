---
UID: NN:evr.IMFVideoPositionMapper
title: IMFVideoPositionMapper
author: windows-sdk-content
description: Maps a position on an input video stream to the corresponding position on an output video stream.
old-location: mf\imfvideopositionmapper.htm
old-project: medfound
ms.assetid: 282fa124-909f-49dc-9a86-3d962193e903
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 282fa124-909f-49dc-9a86-3d962193e903, IMFVideoPositionMapper, IMFVideoPositionMapper interface [Media Foundation], IMFVideoPositionMapper interface [Media Foundation],described, evr/IMFVideoPositionMapper, mf.imfvideopositionmapper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPositionMapper
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoPositionMapper interface


## -description


Maps a position on an input video stream to the corresponding position on an output video stream.

To obtain a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> on the renderer with the service GUID MR_VIDEO_RENDER_SERVICE.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoPositionMapper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoPositionMapper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoPositionMapper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d57aed5f-90cb-47e7-af80-f3573a3b8256">MapOutputCoordinateToInputStream</a>
</td>
<td align="left" width="63%">
Maps output image coordinates to input image coordinates.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

