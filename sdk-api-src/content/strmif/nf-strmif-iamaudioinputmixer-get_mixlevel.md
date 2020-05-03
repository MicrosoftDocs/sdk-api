---
UID: NF:strmif.IAMAudioInputMixer.get_MixLevel
title: IAMAudioInputMixer::get_MixLevel (strmif.h)
description: The get_MixLevel method retrieves the recording level.helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_MixLevel method","IAMAudioInputMixer.get_MixLevel","IAMAudioInputMixer::get_MixLevel","IAMAudioInputMixerget_MixLevel","dshow.iamaudioinputmixer_get_mixlevel","get_MixLevel","get_MixLevel method [DirectShow]","get_MixLevel method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_MixLevel"]
old-location: dshow\iamaudioinputmixer_get_mixlevel.htm
tech.root: DirectShow
ms.assetid: bdf8f90b-72a4-4faf-9d08-2634582245f8
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_MixLevel method, IAMAudioInputMixer.get_MixLevel, IAMAudioInputMixer::get_MixLevel, IAMAudioInputMixerget_MixLevel, dshow.iamaudioinputmixer_get_mixlevel, get_MixLevel, get_MixLevel method [DirectShow], get_MixLevel method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_MixLevel
f1_keywords:
- strmif/IAMAudioInputMixer.get_MixLevel
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
- IAMAudioInputMixer.get_MixLevel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMAudioInputMixer::get_MixLevel


## -description



The <code>get_MixLevel</code> method retrieves the recording level.




## -parameters




### -param pLevel [out]

Receives the recording level. The following values are possible.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0.0 to 1.0</td>
<td>Zero indicates that the recording level is off; the value 1.0 indicates that the recording level is at full volume. Intermediate values are also allowed.</td>
</tr>
<tr>
<td>AMF_AUTOMATICGAIN</td>
<td>Automatic adjustment of the recording level is enabled.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_mixlevel">IAMAudioInputMixer::put_MixLevel</a>
 

 

