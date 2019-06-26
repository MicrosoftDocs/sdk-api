---
UID: NN:mfmediaengine.IMFTimedTextRegion
title: IMFTimedTextRegion (mfmediaengine.h)
author: windows-sdk-content
description: Represents the display region of a timed-text object.
old-location: mf\imftimedtextregion.htm
tech.root: medfound
ms.assetid: 1A6E068F-2E01-4A72-8BCF-D645B1D21ECF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTimedTextRegion, IMFTimedTextRegion interface [Media Foundation], IMFTimedTextRegion interface [Media Foundation],described, mf.imftimedtextregion, mfmediaengine/IMFTimedTextRegion
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFTimedTextRegion"
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFTimedTextRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextRegion interface


## -description


Represents the display region  of a timed-text object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextRegion</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimedTextRegion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextRegion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getbackgroundcolor">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Gets the background color of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getclipoverflow">GetClipOverflow</a>
</td>
<td align="left" width="63%">
Determines whether a clip of text overflowed the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getdisplayalignment">GetDisplayAlignment</a>
</td>
<td align="left" width="63%">
Gets the display alignment of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getextent">GetExtent</a>
</td>
<td align="left" width="63%">
Gets the extent of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getlineheight">GetLineHeight</a>
</td>
<td align="left" width="63%">
Gets the height of each line of text in the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getpadding">GetPadding</a>
</td>
<td align="left" width="63%">
Gets the padding that surrounds the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getposition">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the position of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getscrollmode">GetScrollMode</a>
</td>
<td align="left" width="63%">
Gets the scroll mode of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getwrap">GetWrap</a>
</td>
<td align="left" width="63%">
Determines whether the word wrap feature is enabled in the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getwritingmode">GetWritingMode</a>
</td>
<td align="left" width="63%">
Gets the writing mode of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextregion-getzindex">GetZIndex</a>
</td>
<td align="left" width="63%">
Gets the Z-index (depth) of the region.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

