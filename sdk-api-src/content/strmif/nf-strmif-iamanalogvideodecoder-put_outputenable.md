---
UID: NF:strmif.IAMAnalogVideoDecoder.put_OutputEnable
title: IAMAnalogVideoDecoder::put_OutputEnable
author: windows-driver-content
description: The put_OutputEnable method enables or disables the video port bus.
old-location: dshow\iamanalogvideodecoder_put_outputenable.htm
old-project: DirectShow
ms.assetid: 93163db3-ea9a-4383-b382-7d574ef24dfc
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],put_OutputEnable method, IAMAnalogVideoDecoder.put_OutputEnable, IAMAnalogVideoDecoder::put_OutputEnable, IAMAnalogVideoDecoderput_OutputEnable, dshow.iamanalogvideodecoder_put_outputenable, put_OutputEnable, put_OutputEnable method [DirectShow], put_OutputEnable method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::put_OutputEnable
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
-	IAMAnalogVideoDecoder.put_OutputEnable
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoDecoder::put_OutputEnable


## -description



The <code>put_OutputEnable</code> method enables or disables the video port bus.




## -parameters




### -param lOutputEnable [in]

Specifies whether the bus is enabled. Use one of the following values.

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
<td>Disable the video port bus.</td>
</tr>
<tr>
<td>1</td>
<td>Enable the video port bus.</td>
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
 




## -remarks



This method applies only to devices that use a shared video port bus. If the value is 1, the device will actively drive the video port bus. If the value is zero, the device will be tri-stated.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/81d43941-7c81-4220-915f-0b373a7455e5">IAMAnalogVideoDecoder Interface</a>
 

 

