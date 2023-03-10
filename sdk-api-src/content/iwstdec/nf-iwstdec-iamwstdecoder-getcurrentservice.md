---
UID: NF:iwstdec.IAMWstDecoder.GetCurrentService
title: IAMWstDecoder::GetCurrentService (iwstdec.h)
description: Applications use the GetCurrentService method to retrieve the current WST service.
helpviewer_keywords: ["GetCurrentService","GetCurrentService method [DirectShow]","GetCurrentService method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetCurrentService method","IAMWstDecoder.GetCurrentService","IAMWstDecoder::GetCurrentService","IAMWstDecoderGetCurrentService","dshow.iamwstdecoder_getcurrentservice","iwstdec/IAMWstDecoder::GetCurrentService"]
old-location: dshow\iamwstdecoder_getcurrentservice.htm
tech.root: dshow
ms.assetid: d16b3501-efee-48e6-8d5d-d76f206d77ed
ms.date: 12/05/2018
ms.keywords: GetCurrentService, GetCurrentService method [DirectShow], GetCurrentService method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetCurrentService method, IAMWstDecoder.GetCurrentService, IAMWstDecoder::GetCurrentService, IAMWstDecoderGetCurrentService, dshow.iamwstdecoder_getcurrentservice, iwstdec/IAMWstDecoder::GetCurrentService
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
 - IAMWstDecoder::GetCurrentService
 - iwstdec/IAMWstDecoder::GetCurrentService
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
 - IAMWstDecoder.GetCurrentService
---

# IAMWstDecoder::GetCurrentService


## -description

Applications use the <code>GetCurrentService</code> method to retrieve the current WST service.

## -parameters

### -param lpService [out]

Specifies a pointer to an <a href="/previous-versions/windows/desktop/api/iwstdec/ne-iwstdec-am_wst_service">AM_WST_SERVICE</a> enumeration to receive the service currently being used.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AM_WST_SERVICE_None</td>
<td>No service is currently available.</td>
</tr>
<tr>
<td>AM_WST_SERVICE_Text</td>
<td>The service is providing text.</td>
</tr>
<tr>
<td>AM_WST_SERVICE_IDS</td>
<td>The service is providing IDS data.</td>
</tr>
<tr>
<td>AM_WST_SERVICE_Invalid</td>
<td>The service is invalid.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>