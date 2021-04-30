---
UID: NF:strmif.IAMAudioInputMixer.get_Treble
title: IAMAudioInputMixer::get_Treble (strmif.h)
description: The get_Treble method retrieves the treble equalization.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_Treble method","IAMAudioInputMixer.get_Treble","IAMAudioInputMixer::get_Treble","IAMAudioInputMixerget_Treble","dshow.iamaudioinputmixer_get_treble","get_Treble","get_Treble method [DirectShow]","get_Treble method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_Treble"]
old-location: dshow\iamaudioinputmixer_get_treble.htm
tech.root: dshow
ms.assetid: 6876e121-cb04-49f9-aee4-27759f93529b
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Treble method, IAMAudioInputMixer.get_Treble, IAMAudioInputMixer::get_Treble, IAMAudioInputMixerget_Treble, dshow.iamaudioinputmixer_get_treble, get_Treble, get_Treble method [DirectShow], get_Treble method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Treble
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMAudioInputMixer::get_Treble
 - strmif/IAMAudioInputMixer::get_Treble
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAudioInputMixer.get_Treble
---

# IAMAudioInputMixer::get_Treble


## -description

The <code>get_Treble</code> method retrieves the treble equalization.

## -parameters

### -param pTreble [out]

Receives the treble gain, in decibels. A negative value indicates attenuation.

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_treble">IAMAudioInputMixer::put_Treble</a>