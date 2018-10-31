---
UID: NF:il21dec.IAMLine21Decoder.SetDrawBackgroundMode
title: IAMLine21Decoder::SetDrawBackgroundMode
author: windows-sdk-content
description: The SetDrawBackgroundMode method specifies whether the Line 21 Decoder filter draws the captions on a transparent background or an opaque background. By default, the caption background is opaque.
old-location: dshow\iamline21decoder_setdrawbackgroundmode.htm
tech.root: DirectShow
ms.assetid: 56301cc2-8f27-4530-bb6e-9909eb5bb390
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetDrawBackgroundMode method, IAMLine21Decoder.SetDrawBackgroundMode, IAMLine21Decoder::SetDrawBackgroundMode, IAMLine21DecoderSetDrawBackgroundMode, SetDrawBackgroundMode, SetDrawBackgroundMode method [DirectShow], SetDrawBackgroundMode method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setdrawbackgroundmode, il21dec/IAMLine21Decoder::SetDrawBackgroundMode
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
 - IAMLine21Decoder.SetDrawBackgroundMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMLine21Decoder::SetDrawBackgroundMode


## -description



The <code>SetDrawBackgroundMode</code> method specifies whether the <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> filter draws the captions on a transparent background or an opaque background. By default, the caption background is opaque.




## -parameters




### -param Mode

Specifies a member of the <a href="https://msdn.microsoft.com/efd8ee53-702b-45af-a3dc-e6afe26b01c9">AM_LINE21_DRAWBGMODE</a> enumeration.


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/817a47d6-39c4-4186-81d0-ad822814f0ee">IAMLine21Decoder::GetDrawBackgroundMode</a>
 

 

