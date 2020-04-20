---
UID: NF:iwstdec.IAMWstDecoder.SetDrawBackgroundMode
title: IAMWstDecoder::SetDrawBackgroundMode (iwstdec.h)
description: Downstream filters use the SetDrawBackgroundMode method to assign whether the caption text background is to be opaque or transparent.helpviewer_keywords: ["IAMWstDecoder interface [DirectShow]","SetDrawBackgroundMode method","IAMWstDecoder.SetDrawBackgroundMode","IAMWstDecoder::SetDrawBackgroundMode","IAMWstDecoderSetDrawBackgroundMode","SetDrawBackgroundMode","SetDrawBackgroundMode method [DirectShow]","SetDrawBackgroundMode method [DirectShow]","IAMWstDecoder interface","dshow.iamwstdecoder_setdrawbackgroundmode","iwstdec/IAMWstDecoder::SetDrawBackgroundMode"]
old-location: dshow\iamwstdecoder_setdrawbackgroundmode.htm
tech.root: DirectShow
ms.assetid: d237d3dc-b3c9-44b2-9277-798c4830b361
ms.date: 12/05/2018
ms.keywords: IAMWstDecoder interface [DirectShow],SetDrawBackgroundMode method, IAMWstDecoder.SetDrawBackgroundMode, IAMWstDecoder::SetDrawBackgroundMode, IAMWstDecoderSetDrawBackgroundMode, SetDrawBackgroundMode, SetDrawBackgroundMode method [DirectShow], SetDrawBackgroundMode method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setdrawbackgroundmode, iwstdec/IAMWstDecoder::SetDrawBackgroundMode
f1_keywords:
- iwstdec/IAMWstDecoder.SetDrawBackgroundMode
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
- IAMWstDecoder.SetDrawBackgroundMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMWstDecoder::SetDrawBackgroundMode


## -description



Downstream filters use the <code>SetDrawBackgroundMode</code> method to assign whether the caption text background is to be opaque or transparent.




## -parameters




### -param Mode [in]

A member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iwstdec/ne-iwstdec-am_wst_drawbgmode">AM_WST_DRAWBGMODE</a> enumeration that specifies whether the caption text background is to be opaque or transparent.

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
 

 

