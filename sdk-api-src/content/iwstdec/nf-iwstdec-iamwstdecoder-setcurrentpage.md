---
UID: NF:iwstdec.IAMWstDecoder.SetCurrentPage
title: IAMWstDecoder::SetCurrentPage (iwstdec.h)
description: Downstream filters use the SetCurrentPage method to assign the current page.
helpviewer_keywords: ["IAMWstDecoder interface [DirectShow]","SetCurrentPage method","IAMWstDecoder.SetCurrentPage","IAMWstDecoder::SetCurrentPage","IAMWstDecoderSetCurrentPage","SetCurrentPage","SetCurrentPage method [DirectShow]","SetCurrentPage method [DirectShow]","IAMWstDecoder interface","dshow.iamwstdecoder_setcurrentpage","iwstdec/IAMWstDecoder::SetCurrentPage"]
old-location: dshow\iamwstdecoder_setcurrentpage.htm
tech.root: dshow
ms.assetid: 84f8854d-77a7-4ae3-9fec-c4d6fce7eead
ms.date: 12/05/2018
ms.keywords: IAMWstDecoder interface [DirectShow],SetCurrentPage method, IAMWstDecoder.SetCurrentPage, IAMWstDecoder::SetCurrentPage, IAMWstDecoderSetCurrentPage, SetCurrentPage, SetCurrentPage method [DirectShow], SetCurrentPage method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setcurrentpage, iwstdec/IAMWstDecoder::SetCurrentPage
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
 - IAMWstDecoder::SetCurrentPage
 - iwstdec/IAMWstDecoder::SetCurrentPage
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
 - IAMWstDecoder.SetCurrentPage
---

# IAMWstDecoder::SetCurrentPage


## -description

Downstream filters use the <code>SetCurrentPage</code> method to assign the current page.

## -parameters

### -param WstPage [in]

Specifies an <a href="/previous-versions/windows/desktop/api/iwstdec/ns-iwstdec-am_wst_page">AM_WST_PAGE</a> structure that is used to assign the current page.

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>