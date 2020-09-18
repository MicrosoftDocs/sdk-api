---
UID: NN:iwstdec.IAMWstDecoder
title: IAMWstDecoder (iwstdec.h)
description: The IAMWstDecoder interface sets and retrieves information about World Standard Teletext (WST). The WST Decoder filter implements this interface.
helpviewer_keywords: ["IAMWstDecoder","IAMWstDecoder interface [DirectShow]","IAMWstDecoder interface [DirectShow]","described","IAMWstDecoderInterface","dshow.iamwstdecoder","iwstdec/IAMWstDecoder"]
old-location: dshow\iamwstdecoder.htm
tech.root: dshow
ms.assetid: f2f5a459-14de-4be1-909c-3c23e4cfd737
ms.date: 12/05/2018
ms.keywords: IAMWstDecoder, IAMWstDecoder interface [DirectShow], IAMWstDecoder interface [DirectShow],described, IAMWstDecoderInterface, dshow.iamwstdecoder, iwstdec/IAMWstDecoder
req.header: iwstdec.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMWstDecoder
 - iwstdec/IAMWstDecoder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMWstDecoder
---

# IAMWstDecoder interface


## -description

The <code>IAMWstDecoder</code> interface sets and retrieves information about World Standard Teletext (WST). The <a href="/windows/desktop/DirectShow/wst-decoder-filter">WST Decoder</a> filter implements this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMWstDecoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMWstDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMWstDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getanswermode">GetAnswerMode</a>
</td>
<td align="left" width="63%">
Retrieves whether hidden text is exposed or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getbackgroundcolor">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the current physical color used in color keying the background for overlay mixing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getcurrentpage">GetCurrentPage</a>
</td>
<td align="left" width="63%">
Retrieves the current WST page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getcurrentservice">GetCurrentService</a>
</td>
<td align="left" width="63%">
Retrieves the current WST service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getdecoderlevel">GetDecoderLevel</a>
</td>
<td align="left" width="63%">
Retrieves the WST decoder level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getdrawbackgroundmode">GetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Determines whether the caption text background is opaque or transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getholdpage">GetHoldPage</a>
</td>
<td align="left" width="63%">
Determines whether the current WST page is held by the WST decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getoutputformat">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current output video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getredrawalways">GetRedrawAlways</a>
</td>
<td align="left" width="63%">
Retrieves whether the whole output bitmap should be redrawn for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-getservicestate">GetServiceState</a>
</td>
<td align="left" width="63%">
Retrieves whether closed captioning is on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setanswermode">SetAnswerMode</a>
</td>
<td align="left" width="63%">
Assigns whether hidden text is exposed or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setbackgroundcolor">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Assigns the current physical color used in color keying the background for overlay mixing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setcurrentpage">SetCurrentPage</a>
</td>
<td align="left" width="63%">
Assigns the current WST page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setdrawbackgroundmode">SetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Assigns the caption text background to be opaque or transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setholdpage">SetHoldPage</a>
</td>
<td align="left" width="63%">
Instructs the WST decoder to hold the current page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setoutputformat">SetOutputFormat</a>
</td>
<td align="left" width="63%">
Assigns an output video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setredrawalways">SetRedrawAlways</a>
</td>
<td align="left" width="63%">
Sets whether the whole output bitmap should be redrawn for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwstdec/nf-iwstdec-iamwstdecoder-setservicestate">SetServiceState</a>
</td>
<td align="left" width="63%">
Sets closed captioning on or off.

</td>
</tr>
</table>