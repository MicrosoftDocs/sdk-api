---
UID: NF:strmif.IAMAnalogVideoEncoder.get_CCEnable
title: IAMAnalogVideoEncoder::get_CCEnable
author: windows-sdk-content
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The get_CCEnable determines whether closed captioning on the encoder is currently enabled.
old-location: dshow\iamanalogvideoencoder_get_ccenable.htm
old-project: DirectShow
ms.assetid: 0dab4b3a-f139-4ac5-ab30-f223e9120c44
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],get_CCEnable method, IAMAnalogVideoEncoder.get_CCEnable, IAMAnalogVideoEncoder::get_CCEnable, IAMAnalogVideoEncoderget_CCEnable, dshow.iamanalogvideoencoder_get_ccenable, get_CCEnable, get_CCEnable method [DirectShow], get_CCEnable method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::get_CCEnable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAnalogVideoEncoder.get_CCEnable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoEncoder::get_CCEnable


## -description



<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>get_CCEnable</code> determines whether closed captioning on the encoder is currently enabled.




## -parameters




### -param lCCEnable [out]

Specifies a pointer to a long integer to receive the current status of closed captioning on the encoder.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>1</td>
<td>Closed captioning enabled.</td>
</tr>
<tr>
<td>0</td>
<td>Closed captioning disabled.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fb2927cf-c979-411f-a896-d010b684acf2">IAMAnalogVideoEncoder Interface</a>
 

 

