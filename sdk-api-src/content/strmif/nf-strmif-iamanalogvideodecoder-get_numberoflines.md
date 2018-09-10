---
UID: NF:strmif.IAMAnalogVideoDecoder.get_NumberOfLines
title: IAMAnalogVideoDecoder::get_NumberOfLines
author: windows-sdk-content
description: The get_NumberOfLInes method retrieves the number of scan lines in the video signal.
old-location: dshow\iamanalogvideodecoder_get_numberoflines.htm
tech.root: DirectShow
ms.assetid: d1c30230-bd47-4bdb-a89a-332c4da7cc00
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_NumberOfLines method, IAMAnalogVideoDecoder.get_NumberOfLines, IAMAnalogVideoDecoder::get_NumberOfLines, IAMAnalogVideoDecoderget_NumberOfLines, dshow.iamanalogvideodecoder_get_numberoflines, get_NumberOfLines, get_NumberOfLines method [DirectShow], get_NumberOfLines method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_NumberOfLines
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
 - IAMAnalogVideoDecoder.get_NumberOfLines
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAnalogVideoDecoder::get_NumberOfLines


## -description



The <code>get_NumberOfLInes</code> method retrieves the number of scan lines in the video signal.




## -parameters




### -param plNumberOfLines [out]

Pointer to a variable that receives the number of scan lines in the video signal. This is generally by 525 lines for NTSC and 625 lines for PAL or SECAM.


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
 

 

