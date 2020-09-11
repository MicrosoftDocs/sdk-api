---
UID: NN:evr.IMFVideoPositionMapper
title: IMFVideoPositionMapper (evr.h)
description: Maps a position on an input video stream to the corresponding position on an output video stream.
helpviewer_keywords: ["282fa124-909f-49dc-9a86-3d962193e903","IMFVideoPositionMapper","IMFVideoPositionMapper interface [Media Foundation]","IMFVideoPositionMapper interface [Media Foundation]","described","evr/IMFVideoPositionMapper","mf.imfvideopositionmapper"]
old-location: mf\imfvideopositionmapper.htm
tech.root: mf
ms.assetid: 282fa124-909f-49dc-9a86-3d962193e903
ms.date: 12/05/2018
ms.keywords: 282fa124-909f-49dc-9a86-3d962193e903, IMFVideoPositionMapper, IMFVideoPositionMapper interface [Media Foundation], IMFVideoPositionMapper interface [Media Foundation],described, evr/IMFVideoPositionMapper, mf.imfvideopositionmapper
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoPositionMapper
 - evr/IMFVideoPositionMapper
dev_langs:
 - c++
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
---

# IMFVideoPositionMapper interface


## -description

Maps a position on an input video stream to the corresponding position on an output video stream.

To obtain a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the renderer with the service GUID MR_VIDEO_RENDER_SERVICE.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoPositionMapper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoPositionMapper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideopositionmapper-mapoutputcoordinatetoinputstream">MapOutputCoordinateToInputStream</a>
</td>
<td align="left" width="63%">
Maps output image coordinates to input image coordinates.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

