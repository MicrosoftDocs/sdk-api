---
UID: NN:strmif.IAMTVAudio
title: IAMTVAudio (strmif.h)
description: The IAMTVAudio interface controls audio from a television source. The TV Audio filter implements this interface. Applications can use it to control television audio settings, including secondary audio program (SAP) and stereo or mono selection.
helpviewer_keywords: ["IAMTVAudio","IAMTVAudio interface [DirectShow]","IAMTVAudio interface [DirectShow]","described","IAMTVAudioInterface","dshow.iamtvaudio","strmif/IAMTVAudio"]
old-location: dshow\iamtvaudio.htm
tech.root: DirectShow
ms.assetid: de340594-4410-4896-b206-0f47d4035bc1
ms.date: 12/05/2018
ms.keywords: IAMTVAudio, IAMTVAudio interface [DirectShow], IAMTVAudio interface [DirectShow],described, IAMTVAudioInterface, dshow.iamtvaudio, strmif/IAMTVAudio
f1_keywords:
- strmif/IAMTVAudio
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
- IAMTVAudio
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTVAudio interface


## -description



The <code>IAMTVAudio</code> interface controls audio from a television source. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/tv-audio-filter">TV Audio</a> filter implements this interface. Applications can use it to control television audio settings, including secondary audio program (SAP) and stereo or mono selection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTVAudio</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTVAudio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTVAudio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvaudio-get_tvaudiomode">get_TVAudioMode</a>
</td>
<td align="left" width="63%">
Retrieves the current TV audio mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvaudio-getavailabletvaudiomodes">GetAvailableTVAudioModes</a>
</td>
<td align="left" width="63%">
Retrieves a bitmask of the possible modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvaudio-gethardwaresupportedtvaudiomodes">GetHardwareSupportedTVAudioModes</a>
</td>
<td align="left" width="63%">
Retrieves a bitmask of the formats available in the hardware.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvaudio-put_tvaudiomode">put_TVAudioMode</a>
</td>
<td align="left" width="63%">
Sets the current TV audio mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvaudio-registernotificationcallback">RegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvaudio-unregisternotificationcallback">UnRegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/analog-television">Analog Television</a>
 

 

