---
UID: NN:amaudio.IAMDirectSound
title: IAMDirectSound (amaudio.h)
description: The IAMDirectSound interface specifies which window has focus for controlling DirectSound audio playback.helpviewer_keywords: ["IAMDirectSound","IAMDirectSound interface [DirectShow]","IAMDirectSound interface [DirectShow]","described","IAMDirectSoundInterface","amaudio/IAMDirectSound","dshow.iamdirectsound"]
old-location: dshow\iamdirectsound.htm
tech.root: DirectShow
ms.assetid: a9afaeb7-e2d4-4dbf-9f4d-144cafbd5e28
ms.date: 12/05/2018
ms.keywords: IAMDirectSound, IAMDirectSound interface [DirectShow], IAMDirectSound interface [DirectShow],described, IAMDirectSoundInterface, amaudio/IAMDirectSound, dshow.iamdirectsound
f1_keywords:
- amaudio/IAMDirectSound
dev_langs:
- c++
req.header: amaudio.h
req.include-header: 
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
- IAMDirectSound
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDirectSound interface


## -description



The <code>IAMDirectSound</code> interface specifies which window has focus for controlling DirectSound audio playback. DirectShow provides limited support for this interface:

<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> implements the <b>GetFocusWindow</b> and <b>SetFocusWindow</b> methods. It does not implement the other methods on the interface.</li>
<li>The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> exposes the interface but does not implement any of its methods.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDirectSound</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDirectSound</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDirectSound</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-getdirectsoundinterface">GetDirectSoundInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-getfocuswindow">GetFocusWindow</a>
</td>
<td align="left" width="63%">
Retrieves the window that is handling sound playback for the current media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-getprimarybufferinterface">GetPrimaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-getsecondarybufferinterface">GetSecondaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-releasedirectsoundinterface">ReleaseDirectSoundInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-releaseprimarybufferinterface">ReleasePrimaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-releasesecondarybufferinterface">ReleaseSecondaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nf-amaudio-iamdirectsound-setfocuswindow">SetFocusWindow</a>
</td>
<td align="left" width="63%">
Sets the window that will handle sound playback for the current media file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

