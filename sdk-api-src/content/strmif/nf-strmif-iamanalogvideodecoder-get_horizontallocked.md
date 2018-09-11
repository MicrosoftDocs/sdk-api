---
UID: NF:strmif.IAMAnalogVideoDecoder.get_HorizontalLocked
title: IAMAnalogVideoDecoder::get_HorizontalLocked
author: windows-sdk-content
description: The get_HorizontalLocked method determines whether the horizontal sync is locked.
old-location: dshow\iamanalogvideodecoder_get_horizontallocked.htm
tech.root: DirectShow
ms.assetid: c3923440-8770-42f1-a8f3-afa2e8a512d5
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_HorizontalLocked method, IAMAnalogVideoDecoder.get_HorizontalLocked, IAMAnalogVideoDecoder::get_HorizontalLocked, IAMAnalogVideoDecoderget_HorizontalLocked, dshow.iamanalogvideodecoder_get_horizontallocked, get_HorizontalLocked, get_HorizontalLocked method [DirectShow], get_HorizontalLocked method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_HorizontalLocked
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMAnalogVideoDecoder.get_HorizontalLocked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAnalogVideoDecoder::get_HorizontalLocked


## -description



The <code>get_HorizontalLocked</code> method determines whether the horizontal sync is locked.




## -parameters




### -param plLocked [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Horizontal sync is not locked.</td>
</tr>
<tr>
<td>1</td>
<td>Horizontal sync is locked</td>
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
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/81d43941-7c81-4220-915f-0b373a7455e5">IAMAnalogVideoDecoder Interface</a>
 

 

