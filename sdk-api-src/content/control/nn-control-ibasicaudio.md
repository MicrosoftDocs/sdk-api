---
UID: NN:control.IBasicAudio
title: IBasicAudio (control.h)

description: The IBasicAudio interface controls the volume and balance of the audio stream.This interface is implemented on the Audio Renderer (WaveOut) filter and the DirectSound Renderer filter, but is exposed to applications through the Filter Graph Manager.
old-location: dshow\ibasicaudio.htm
tech.root: DirectShow
ms.assetid: 0335b263-8d32-4690-a606-ba2b3e382680

ms.date: 12/05/2018
ms.keywords: IBasicAudio, IBasicAudio interface [DirectShow], IBasicAudio interface [DirectShow],described, IBasicAudioInterface, control/IBasicAudio, dshow.ibasicaudio
ms.topic: interface
f1_keywords: 
 - "control/IBasicAudio"
dev_langs:
 - c++
req.header: control.h
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
 - IBasicAudio
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBasicAudio interface


## -description



The <code>IBasicAudio</code> interface controls the volume and balance of the audio stream.

This interface is implemented on the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> filter and the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> filter, but is exposed to applications through the Filter Graph Manager. Applications should always retrieve this interface from the Filter Graph Manager.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBasicAudio</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBasicAudio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBasicAudio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicaudio-get_balance">get_Balance</a>
</td>
<td align="left" width="63%">
Retrieves the balance for the audio signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicaudio-get_volume">get_Volume</a>
</td>
<td align="left" width="63%">
Retrieves the volume (amplitude) of the audio signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicaudio-put_balance">put_Balance</a>
</td>
<td align="left" width="63%">
Sets the balance for the audio signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicaudio-put_volume">put_Volume</a>
</td>
<td align="left" width="63%">
Sets the volume (amplitude) of the audio signal.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

