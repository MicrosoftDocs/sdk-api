---
UID: NF:strmif.IAMAudioInputMixer.put_Bass
title: IAMAudioInputMixer::put_Bass
author: windows-sdk-content
description: The put_Bass method sets the bass equalization.
old-location: dshow\iamaudioinputmixer_put_bass.htm
tech.root: DirectShow
ms.assetid: cf752767-826d-487d-ae05-9737765975c8
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Bass method, IAMAudioInputMixer.put_Bass, IAMAudioInputMixer::put_Bass, IAMAudioInputMixerput_Bass, dshow.iamaudioinputmixer_put_bass, put_Bass, put_Bass method [DirectShow], put_Bass method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Bass
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
 - IAMAudioInputMixer.put_Bass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioInputMixer::put_Bass


## -description



The <code>put_Bass</code> method sets the bass equalization.




## -parameters




### -param Bass [in]

Specifies the gain, in decibels. A negative value specifies attenuation.


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
Invalid argument. Must be in range given by <a href="https://msdn.microsoft.com/e0a77f8c-8608-4e16-bc7a-3c90dde2aad8">IAMAudioInputMixer::get_BassRange</a>.

</td>
</tr>
</table>
 




## -remarks



This method boosts or cuts the signal's bass before it is recorded, by the number of decibels specified in the <i>Bass</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/08edf6be-81b7-4402-a500-1b7d9c389042">IAMAudioInputMixer::get_Bass</a>
 

 

