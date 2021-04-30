---
UID: NF:iwstdec.IAMWstDecoder.GetHoldPage
title: IAMWstDecoder::GetHoldPage (iwstdec.h)
description: Downstream filters use the GetHoldPage method to determine whether the current WST page is held. When the WST decoder holds a page, any updates from the TV stream are turned off. It is though the page was paused in real time.
helpviewer_keywords: ["GetHoldPage","GetHoldPage method [DirectShow]","GetHoldPage method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetHoldPage method","IAMWstDecoder.GetHoldPage","IAMWstDecoder::GetHoldPage","IAMWstDecoderGetHoldPage","dshow.iamwstdecoder_getholdpage","iwstdec/IAMWstDecoder::GetHoldPage"]
old-location: dshow\iamwstdecoder_getholdpage.htm
tech.root: dshow
ms.assetid: db09b2a2-7f92-421a-8582-4ed648563119
ms.date: 12/05/2018
ms.keywords: GetHoldPage, GetHoldPage method [DirectShow], GetHoldPage method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetHoldPage method, IAMWstDecoder.GetHoldPage, IAMWstDecoder::GetHoldPage, IAMWstDecoderGetHoldPage, dshow.iamwstdecoder_getholdpage, iwstdec/IAMWstDecoder::GetHoldPage
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
 - IAMWstDecoder::GetHoldPage
 - iwstdec/IAMWstDecoder::GetHoldPage
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
 - IAMWstDecoder.GetHoldPage
---

# IAMWstDecoder::GetHoldPage


## -description

Downstream filters use the <code>GetHoldPage</code> method to determine whether the current WST page is held. When the WST decoder holds a page, any updates from the TV stream are turned off. It is though the page was paused in real time.

## -parameters

### -param pbHoldPage [out]

Pointer to a <b>BOOL</b> to receive the status of the WST page.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The current page is held.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The current page is not held.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>