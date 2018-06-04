---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMpegAudioDecoder::get_DualMode


## -description



Returns which channel is currently being decoded.




## -parameters




### -param pIntDecode [out]

Indicates the channel(s) to be decoded.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The <i>pIntDecode</i> parameter can have one of the values in the following table.

<table>
<tr>
<th>
              Constant
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td><b>
              AM_MPEG_AUDIO_DUAL_MERGE
            </b></td>
<td>Both channels are decoded.</td>
</tr>
<tr>
<td><b>
              AM_MPEG_AUDIO_DUAL_LEFT
            </b></td>
<td>The left channel is decoded.</td>
</tr>
<tr>
<td><b>
              AM_MPEG_AUDIO_DUAL_RIGHT
            </b></td>
<td>The right channel is decoded.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/59fd96ef-2f9a-4a8e-bd08-2695de52b1c6">IMpegAudioDecoder</a>
 

 

