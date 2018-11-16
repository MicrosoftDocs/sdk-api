---
UID: NF:il21dec.IAMLine21Decoder.GetRedrawAlways
title: IAMLine21Decoder::GetRedrawAlways
author: windows-sdk-content
description: The GetRedrawAlways method indicates whether the Line 21 Decoder filter redraws the entire output bitmap for each sample.
old-location: dshow\iamline21decoder_getredrawalways.htm
tech.root: DirectShow
ms.assetid: 9ab65d23-816d-4c6f-a0bc-b3334babdc23
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRedrawAlways, GetRedrawAlways method [DirectShow], GetRedrawAlways method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetRedrawAlways method, IAMLine21Decoder.GetRedrawAlways, IAMLine21Decoder::GetRedrawAlways, IAMLine21DecoderGetRedrawAlways, dshow.iamline21decoder_getredrawalways, il21dec/IAMLine21Decoder::GetRedrawAlways
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
 - IAMLine21Decoder.GetRedrawAlways
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- il21dec.h
: 
- IAMLine21Decoder.GetRedrawAlways
: 
---

# IAMLine21Decoder::GetRedrawAlways


## -description



The <code>GetRedrawAlways</code> method indicates whether the <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> filter redraws the entire output bitmap for each sample.




## -parameters




### -param lpbOption

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The filter always redraws the entire bitmap.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The filter does not always redraw the entire bitmap. (Default)</td>
</tr>
</table>
 


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



<a href="https://msdn.microsoft.com/b6fbb5c3-28af-4db6-8dc4-82271b69bf71">IAMLine21Decoder Interface</a>



<a href="https://msdn.microsoft.com/20f2e95a-8362-457d-b562-f7263e698551">IAMLine21Decoder::SetRedrawAlways</a>
 

 

