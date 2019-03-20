---
UID: NN:mfmediaengine.IMFTimedTextRegion
title: IMFTimedTextRegion (mfmediaengine.h)
author: windows-sdk-content
description: Represents the display region of a timed-text object.
old-location: mf\imftimedtextregion.htm
tech.root: medfound
ms.assetid: 1A6E068F-2E01-4A72-8BCF-D645B1D21ECF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFTimedTextRegion, IMFTimedTextRegion interface [Media Foundation], IMFTimedTextRegion interface [Media Foundation],described, mf.imftimedtextregion, mfmediaengine/IMFTimedTextRegion
ms.topic: interface
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
---

# IMFTimedTextRegion interface


## -description


Represents the display region  of a timed-text object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextRegion</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimedTextRegion</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E92FFB7E-C364-43C8-82CF-C3B4116C4187">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Gets the background color of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F48D4F1C-E00C-40BE-B292-B92C5B214F56">GetClipOverflow</a>
</td>
<td align="left" width="63%">
Determines whether a clip of text overflowed the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CE2A9014-5510-4648-85F8-4A64C04C9F0C">GetDisplayAlignment</a>
</td>
<td align="left" width="63%">
Gets the display alignment of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/581D9A8D-FBED-4E67-9E81-77D9C29ADF82">GetExtent</a>
</td>
<td align="left" width="63%">
Gets the extent of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41514FCA-5C2A-48E5-A9F8-72B5B9160CD6">GetLineHeight</a>
</td>
<td align="left" width="63%">
Gets the height of each line of text in the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B3C07CF-0E9C-4C7D-8F41-7A0B168967A3">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B97ECFD8-2E96-425F-B29E-49E7D53BBFCB">GetPadding</a>
</td>
<td align="left" width="63%">
Gets the padding that surrounds the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1DEE0689-A428-4121-9ED5-5E4D1376461E">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the position of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85CD2A7A-23ED-4D5C-AAEC-D5DF9F059897">GetScrollMode</a>
</td>
<td align="left" width="63%">
Gets the scroll mode of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/634B686C-A083-4F11-9330-4BD22D93A066">GetWrap</a>
</td>
<td align="left" width="63%">
Determines whether the word wrap feature is enabled in the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCF99D3C-554A-4788-B54B-236F463B1EAE">GetWritingMode</a>
</td>
<td align="left" width="63%">
Gets the writing mode of the region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/662A5D79-7FCE-45D3-BCB1-5DE08DC0F981">GetZIndex</a>
</td>
<td align="left" width="63%">
Gets the Z-index (depth) of the region.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

