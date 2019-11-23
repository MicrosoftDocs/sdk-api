---
UID: NN:wmcodecdsp.IWMResizerProps
title: IWMResizerProps (wmcodecdsp.h)

description: Sets properties on the video resizer DSP.
old-location: mf\iwmresizerpropsinterface.htm
tech.root: medfound
ms.assetid: 12c26507-c729-4143-a0bd-e043d42744f6

ms.date: 12/05/2018
ms.keywords: IWMResizerProps, IWMResizerProps interface [Media Foundation], IWMResizerProps interface [Media Foundation],described, codecapi.iwmresizerpropsinterface, mf.iwmresizerprops, mf.iwmresizerpropsinterface, wmcodecdsp/IWMResizerProps
ms.topic: interface
f1_keywords: 
 - "wmcodecdsp/IWMResizerProps"
dev_langs:
 - c++
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - wmcodecdsp.h
api_name:
 - IWMResizerProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMResizerProps interface


## -description


Sets properties on the video resizer DSP.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMResizerProps</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMResizerProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMResizerProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresizerprops-getfullcropregion">GetFullCropRegion</a>
</td>
<td align="left" width="63%">
Retrieves the source and destination rectangles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresizerprops-setclipregion">SetClipRegion</a>
</td>
<td align="left" width="63%">
Sets the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresizerprops-setfullcropregion">SetFullCropRegion</a>
</td>
<td align="left" width="63%">
Sets the source and destination rectangles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresizerprops-setinterlacemode">SetInterlaceMode</a>
</td>
<td align="left" width="63%">
Specifies whether the input video stream is interlaced.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresizerprops-setresizerquality">SetResizerQuality</a>
</td>
<td align="left" width="63%">
Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/videoresizer">Video Resizer DSP</a>
 

 

