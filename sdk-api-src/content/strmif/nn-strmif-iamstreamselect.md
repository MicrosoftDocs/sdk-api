---
UID: NN:strmif.IAMStreamSelect
title: IAMStreamSelect (strmif.h)
description: The IAMStreamSelect interface selects from the available streams on a parser filter.
old-location: dshow\iamstreamselect.htm
tech.root: DirectShow
ms.assetid: a305e91e-f506-4bd1-b4d4-7361df89e158
ms.date: 12/05/2018
ms.keywords: IAMStreamSelect, IAMStreamSelect interface [DirectShow], IAMStreamSelect interface [DirectShow],described, IAMStreamSelectInterface, dshow.iamstreamselect, strmif/IAMStreamSelect
f1_keywords:
- strmif/IAMStreamSelect
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMStreamSelect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMStreamSelect interface


## -description



The <code>IAMStreamSelect</code> interface selects from the available streams on a parser filter. For example, a file might contain audio streams encoded in several languages, such as English, German, and French. The application could use this interface to select which language is played.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStreamSelect</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMStreamSelect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMStreamSelect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamstreamselect-count">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of available streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamstreamselect-enable">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables a given stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamstreamselect-info">Info</a>
</td>
<td align="left" width="63%">
Retrieves information about a given stream.

</td>
</tr>
</table> 


## -remarks



The following filters implement this interface:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-1-stream-splitter-filter">MPEG-1 Stream Splitter</a> filter</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-2-splitter">MPEG-2 Splitter</a> filter</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/DirectShow/sami--cc--parser-filter">SAMI (CC) Parser</a> filter</li>
</ul>


