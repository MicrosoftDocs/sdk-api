---
UID: NN:evr.IEVRFilterConfigEx
title: IEVRFilterConfigEx (evr.h)
description: Configures the DirectShow Enhanced Video Renderer (EVR) filter.
helpviewer_keywords: ["IEVRFilterConfigEx","IEVRFilterConfigEx interface [Media Foundation]","IEVRFilterConfigEx interface [Media Foundation]","described","evr/IEVRFilterConfigEx","mf.ievrfilterconfigex"]
old-location: mf\ievrfilterconfigex.htm
tech.root: mf
ms.assetid: bbe85dc1-af9c-4be7-9064-d61bba160942
ms.date: 12/05/2018
ms.keywords: IEVRFilterConfigEx, IEVRFilterConfigEx interface [Media Foundation], IEVRFilterConfigEx interface [Media Foundation],described, evr/IEVRFilterConfigEx, mf.ievrfilterconfigex
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRFilterConfigEx
 - evr/IEVRFilterConfigEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IEVRFilterConfigEx
---

# IEVRFilterConfigEx interface


## -description

Configures the DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer</a> (EVR) filter.  To get a pointer to this interface, call <b>QueryInterface</b> on the  EVR filter.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEVRFilterConfigEx</b> interface inherits from <a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig">IEVRFilterConfig</a>. <b>IEVRFilterConfigEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEVRFilterConfigEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-getconfigprefs">GetConfigPrefs</a>
</td>
<td align="left" width="63%">
Gets the configuration parameters for the  DirectShow EVR filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs">SetConfigPrefs</a>
</td>
<td align="left" width="63%">
Sets the configuration parameters for the DirectShow EVR filter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig">IEVRFilterConfig</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>