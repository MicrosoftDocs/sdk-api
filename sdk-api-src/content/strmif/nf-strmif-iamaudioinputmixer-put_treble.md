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

# IAMAudioInputMixer::put_Treble


## -description



The <code>put_Treble</code> method sets the treble equalization for this input.




## -parameters




### -param Treble [in]

Specifies the gain, in decibels. A negative value specifies attenuation.


## -returns



Returns an <b>HRESULT</b> value. The following are possible values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid. Must be in range given by <a href="https://msdn.microsoft.com/726cbdda-5772-43bc-846f-f7d1672cc56f">IAMAudioInputMixer::get_TrebleRange</a>.

</td>
</tr>
</table>
 




## -remarks



This method boosts or cuts the signal's treble by a specified number of decibels before it is recorded.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/6876e121-cb04-49f9-aee4-27759f93529b">IAMAudioInputMixer::get_Treble</a>
 

 

