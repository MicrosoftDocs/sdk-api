---
UID: NF:il21dec.IAMLine21Decoder.GetDecoderLevel
title: IAMLine21Decoder::GetDecoderLevel
author: windows-driver-content
description: The GetDecoderLevel method retrieves the closed-captioned decoder level.
old-location: dshow\iamline21decoder_getdecoderlevel.htm
old-project: DirectShow
ms.assetid: 6f0fc2c3-cc98-4646-ada0-57d74c6b5dd9
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetDecoderLevel, GetDecoderLevel method [DirectShow], GetDecoderLevel method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetDecoderLevel method, IAMLine21Decoder.GetDecoderLevel, IAMLine21Decoder::GetDecoderLevel, IAMLine21DecoderGetDecoderLevel, dshow.iamline21decoder_getdecoderlevel, il21dec/IAMLine21Decoder::GetDecoderLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: il21dec.h
req.include-header: 
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
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMLine21Decoder.GetDecoderLevel
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMLine21Decoder::GetDecoderLevel


## -description



The <code>GetDecoderLevel</code> method retrieves the closed-captioned decoder level.




## -parameters




### -param lpLevel

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/ffdedab0-9a47-4599-86c2-07f90d4d87ff">AM_LINE21_CCLEVEL</a> enumeration. The returned value is always <b>AM_L21_CCLEVEL_TC2</b> (TeleCaption II).


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



TeleCaption I and TeleCaption II are standards for closed caption decoders. The <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> filter supports TeleCaption II, which is backward compatible with TeleCaption I.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b6fbb5c3-28af-4db6-8dc4-82271b69bf71">IAMLine21Decoder Interface</a>
 

 

