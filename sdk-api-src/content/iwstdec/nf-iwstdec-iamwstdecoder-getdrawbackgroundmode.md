---
UID: NF:iwstdec.IAMWstDecoder.GetDrawBackgroundMode
title: IAMWstDecoder::GetDrawBackgroundMode (iwstdec.h)
description: Downstream filters use the GetDrawBackgroundMode method to determine whether the caption text background is opaque or transparent.helpviewer_keywords: ["GetDrawBackgroundMode","GetDrawBackgroundMode method [DirectShow]","GetDrawBackgroundMode method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetDrawBackgroundMode method","IAMWstDecoder.GetDrawBackgroundMode","IAMWstDecoder::GetDrawBackgroundMode","IAMWstDecoderGetDrawBackgroundMode","dshow.iamwstdecoder_getdrawbackgroundmode","iwstdec/IAMWstDecoder::GetDrawBackgroundMode"]
old-location: dshow\iamwstdecoder_getdrawbackgroundmode.htm
tech.root: DirectShow
ms.assetid: c5bf3a83-5f74-4ef1-81b6-6c99e3832725
ms.date: 12/05/2018
ms.keywords: GetDrawBackgroundMode, GetDrawBackgroundMode method [DirectShow], GetDrawBackgroundMode method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetDrawBackgroundMode method, IAMWstDecoder.GetDrawBackgroundMode, IAMWstDecoder::GetDrawBackgroundMode, IAMWstDecoderGetDrawBackgroundMode, dshow.iamwstdecoder_getdrawbackgroundmode, iwstdec/IAMWstDecoder::GetDrawBackgroundMode
f1_keywords:
- iwstdec/IAMWstDecoder.GetDrawBackgroundMode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMWstDecoder.GetDrawBackgroundMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMWstDecoder::GetDrawBackgroundMode


## -description



Downstream filters use the <code>GetDrawBackgroundMode</code> method to determine whether the caption text background is opaque or transparent.




## -parameters




### -param lpMode [out]

Receives a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iwstdec/ne-iwstdec-am_wst_drawbgmode">AM_WST_DRAWBGMODE</a> enumeration. This parameter receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AM_WST_DRAWBGMODE_Opaque</td>
<td>Caption text background is opaque.</td>
</tr>
<tr>
<td>AM_WST_DRAWBGMODE_Transparent</td>
<td>Caption text background is transparent.</td>
</tr>
</table>
 


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>
 

 

