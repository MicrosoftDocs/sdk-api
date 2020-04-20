---
UID: NF:strmif.IAMAudioInputMixer.put_Treble
title: IAMAudioInputMixer::put_Treble (strmif.h)
description: The put_Treble method sets the treble equalization for this input.helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","put_Treble method","IAMAudioInputMixer.put_Treble","IAMAudioInputMixer::put_Treble","IAMAudioInputMixerput_Treble","dshow.iamaudioinputmixer_put_treble","put_Treble","put_Treble method [DirectShow]","put_Treble method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::put_Treble"]
old-location: dshow\iamaudioinputmixer_put_treble.htm
tech.root: DirectShow
ms.assetid: 09030c17-14d0-4af2-9e9e-64a536133b64
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Treble method, IAMAudioInputMixer.put_Treble, IAMAudioInputMixer::put_Treble, IAMAudioInputMixerput_Treble, dshow.iamaudioinputmixer_put_treble, put_Treble, put_Treble method [DirectShow], put_Treble method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Treble
f1_keywords:
- strmif/IAMAudioInputMixer.put_Treble
dev_langs:
- c++
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
- IAMAudioInputMixer.put_Treble
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
Argument is invalid. Must be in range given by <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_treblerange">IAMAudioInputMixer::get_TrebleRange</a>.

</td>
</tr>
</table>
 




## -remarks



This method boosts or cuts the signal's treble by a specified number of decibels before it is recorded.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_treble">IAMAudioInputMixer::get_Treble</a>
 

 

