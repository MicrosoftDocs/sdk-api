---
UID: NF:strmif.IAMAnalogVideoDecoder.get_VCRHorizontalLocking
title: IAMAnalogVideoDecoder::get_VCRHorizontalLocking
author: windows-sdk-content
description: The get_VCRHorizontalLocking method indicates whether the decoder is expecting video from a tape source or a broadcast source.
old-location: dshow\iamanalogvideodecoder_get_vcrhorizontallocking.htm
old-project: DirectShow
ms.assetid: 0b527578-1840-4cb1-b94b-9be27b40fcf4
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_VCRHorizontalLocking method, IAMAnalogVideoDecoder.get_VCRHorizontalLocking, IAMAnalogVideoDecoder::get_VCRHorizontalLocking, IAMAnalogVideoDecoderget_VCRHorizontalLocking, dshow.iamanalogvideodecoder_get_vcrhorizontallocking, get_VCRHorizontalLocking, get_VCRHorizontalLocking method [DirectShow], get_VCRHorizontalLocking method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_VCRHorizontalLocking
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMAnalogVideoDecoder.get_VCRHorizontalLocking
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoDecoder::get_VCRHorizontalLocking


## -description



The <code>get_VCRHorizontalLocking</code> method indicates whether the decoder is expecting video from a tape source or a broadcast source.




## -parameters




### -param plVCRHorizontalLocking [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The decoder is expecting video from a broadcast source.</td>
</tr>
<tr>
<td>1</td>
<td>The decoder is expecting video from a tape source.</td>
</tr>
</table>
 


## -returns



Returns an HRESULT value. Possible values include the following.

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
 




## -remarks



The timing accuracy of synchronization pulses is typically poorer from a tape source than from a broadcast source. If the returned value is 1, the decoder might relax its sync timing standards.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/81d43941-7c81-4220-915f-0b373a7455e5">IAMAnalogVideoDecoder Interface</a>
 

 

