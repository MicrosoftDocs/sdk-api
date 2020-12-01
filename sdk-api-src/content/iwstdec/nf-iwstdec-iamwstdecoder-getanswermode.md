---
UID: NF:iwstdec.IAMWstDecoder.GetAnswerMode
title: IAMWstDecoder::GetAnswerMode (iwstdec.h)
description: Downstream filters use the GetAnswerMode method to retrieve the current answer mode.
helpviewer_keywords: ["GetAnswerMode","GetAnswerMode method [DirectShow]","GetAnswerMode method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetAnswerMode method","IAMWstDecoder.GetAnswerMode","IAMWstDecoder::GetAnswerMode","IAMWstDecoderGetAnswerMode","dshow.iamwstdecoder_getanswermode","iwstdec/IAMWstDecoder::GetAnswerMode"]
old-location: dshow\iamwstdecoder_getanswermode.htm
tech.root: dshow
ms.assetid: 6251c9fa-1149-47ac-b776-7d10d153dde5
ms.date: 12/05/2018
ms.keywords: GetAnswerMode, GetAnswerMode method [DirectShow], GetAnswerMode method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetAnswerMode method, IAMWstDecoder.GetAnswerMode, IAMWstDecoder::GetAnswerMode, IAMWstDecoderGetAnswerMode, dshow.iamwstdecoder_getanswermode, iwstdec/IAMWstDecoder::GetAnswerMode
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
 - IAMWstDecoder::GetAnswerMode
 - iwstdec/IAMWstDecoder::GetAnswerMode
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
 - IAMWstDecoder.GetAnswerMode
---

# IAMWstDecoder::GetAnswerMode


## -description

Downstream filters use the <code>GetAnswerMode</code> method to retrieve the current answer mode.

## -parameters

### -param pbAnswer [out]

Receives the current answer mode.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Hidden text exposed.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Hidden text not exposed.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>