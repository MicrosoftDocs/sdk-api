---
UID: NN:strmif.IAMAudioInputMixer
title: IAMAudioInputMixer (strmif.h)
description: The IAMAudioInputMixer interface controls audio capture properties, such as panning and loudness; and enables or disables specific audio inputs, such as the line in or the microphone. The Audio Capture filter exposes this interface on each input pin, as well as on the filter itself. The input pins on the Audio Capture Filter represent physical hardware connections; they are not connected to other DirectShow filters. The pin name indicates the input type; for example, &quot;Line In&quot; or &quot;Microphone.&quot; Use the IAMAudioInputMixer interface as follows:To control the settings on a particular input, use the interface on the pin.To set the overall properties when multiple inputs are enabled, use the interface on the filter.To enable or disable an input, call that pin's IAMAudioInputMixer::put_Enable method.Some methods on this interface might fail, depending on the capabilities of the underlying hardware.Filter Developers:\_Implement this interface on each input pin of an audio capture filter. You can also implement this interface on the audio capture filter itself to control the overall audio settings after mixing.
helpviewer_keywords: ["IAMAudioInputMixer","IAMAudioInputMixer interface [DirectShow]","IAMAudioInputMixer interface [DirectShow]","described","IAMAudioInputMixerInterface","dshow.iamaudioinputmixer","strmif/IAMAudioInputMixer"]
old-location: dshow\iamaudioinputmixer.htm
tech.root: dshow
ms.assetid: 217cb49d-7f5f-42c5-83db-546621f6a375
ms.date: 12/05/2018
ms.keywords: IAMAudioInputMixer, IAMAudioInputMixer interface [DirectShow], IAMAudioInputMixer interface [DirectShow],described, IAMAudioInputMixerInterface, dshow.iamaudioinputmixer, strmif/IAMAudioInputMixer
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
 - IAMAudioInputMixer
 - strmif/IAMAudioInputMixer
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
 - IAMAudioInputMixer
---

# IAMAudioInputMixer interface


## -description

The <code>IAMAudioInputMixer</code> interface controls audio capture properties, such as panning and loudness; and enables or disables specific audio inputs, such as the line in or the microphone.

The <a href="/windows/desktop/DirectShow/audio-capture-filter">Audio Capture</a> filter exposes this interface on each input pin, as well as on the filter itself. The input pins on the Audio Capture Filter represent physical hardware connections; they are not connected to other DirectShow filters. The pin name indicates the input type; for example, "Line In" or "Microphone." Use the <code>IAMAudioInputMixer</code> interface as follows:

<ul>
<li>To control the settings on a particular input, use the interface on the pin.</li>
<li>To set the overall properties when multiple inputs are enabled, use the interface on the filter.</li>
<li>To enable or disable an input, call that pin's <a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_enable">IAMAudioInputMixer::put_Enable</a> method.</li>
</ul>
Some methods on this interface might fail, depending on the capabilities of the underlying hardware.

<b>Filter Developers</b>: Implement this interface on each input pin of an audio capture filter. You can also implement this interface on the audio capture filter itself to control the overall audio settings after mixing.

## -inheritance

The <b>IAMAudioInputMixer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAudioInputMixer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
