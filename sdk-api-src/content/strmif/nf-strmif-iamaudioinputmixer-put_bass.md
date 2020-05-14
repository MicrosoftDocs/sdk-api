---
UID: NF:strmif.IAMAudioInputMixer.put_Bass
title: IAMAudioInputMixer::put_Bass (strmif.h)
description: The put_Bass method sets the bass equalization.helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","put_Bass method","IAMAudioInputMixer.put_Bass","IAMAudioInputMixer::put_Bass","IAMAudioInputMixerput_Bass","dshow.iamaudioinputmixer_put_bass","put_Bass","put_Bass method [DirectShow]","put_Bass method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::put_Bass"]
old-location: dshow\iamaudioinputmixer_put_bass.htm
tech.root: DirectShow
ms.assetid: cf752767-826d-487d-ae05-9737765975c8
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Bass method, IAMAudioInputMixer.put_Bass, IAMAudioInputMixer::put_Bass, IAMAudioInputMixerput_Bass, dshow.iamaudioinputmixer_put_bass, put_Bass, put_Bass method [DirectShow], put_Bass method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Bass
f1_keywords:
- strmif/IAMAudioInputMixer.put_Bass
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
- IAMAudioInputMixer.put_Bass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
Invalid argument. Must be in range given by <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_bassrange">IAMAudioInputMixer::get_BassRange</a>.

</td>
</tr>
</table>
 




## -remarks



This method boosts or cuts the signal's bass before it is recorded, by the number of decibels specified in the <i>Bass</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_bass">IAMAudioInputMixer::get_Bass</a>
 

 

