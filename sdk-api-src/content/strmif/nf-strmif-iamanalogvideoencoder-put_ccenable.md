---
UID: NF:strmif.IAMAnalogVideoEncoder.put_CCEnable
title: IAMAnalogVideoEncoder::put_CCEnable
author: windows-sdk-content
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The put_CCEnable method enables or disables closed captioning.
old-location: dshow\iamanalogvideoencoder_put_ccenable.htm
old-project: DirectShow
ms.assetid: 6513cde7-2765-4225-814b-a619d6a6ab15
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],put_CCEnable method, IAMAnalogVideoEncoder.put_CCEnable, IAMAnalogVideoEncoder::put_CCEnable, IAMAnalogVideoEncoderput_CCEnable, dshow.iamanalogvideoencoder_put_ccenable, put_CCEnable, put_CCEnable method [DirectShow], put_CCEnable method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::put_CCEnable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMAnalogVideoEncoder.put_CCEnable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoEncoder::put_CCEnable


## -description



<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>put_CCEnable</code> method enables or disables closed captioning.




## -parameters




### -param lCCEnable [in]

Specifies whether closed captioning is on or off as a <b>long</b> integer.

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
<td>1</td>
<td>Closed captioning is on.</td>
</tr>
<tr>
<td>0</td>
<td>Closed captioning is off.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fb2927cf-c979-411f-a896-d010b684acf2">IAMAnalogVideoEncoder Interface</a>
 

 

