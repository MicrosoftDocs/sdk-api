---
UID: NN:audioclient.IAudioClient3
title: IAudioClient3 (audioclient.h)
author: windows-sdk-content
description: The IAudioClient3 interface is derived from the IAudioClient2 interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to query for the audio engine's supported periodicities and current periodicity as well as request initialization a shared audio stream with a specified periodicity.
old-location: coreaudio\iaudioclient3.htm
tech.root: CoreAudio
ms.assetid: E8EFE682-E1BC-4D0D-A60E-DD257D6E5894
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioClient3, IAudioClient3 interface [Core Audio], IAudioClient3 interface [Core Audio],described, audioclient/IAudioClient3, coreaudio.iaudioclient3
ms.topic: interface
f1_keywords: 
 - "audioclient/IAudioClient3"
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClient3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioClient3 interface


## -description


The <b>IAudioClient3</b> interface is derived from the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2">IAudioClient2</a> interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to query for the audio engine's supported periodicities and current periodicity as well as request initialization a shared audio stream with a specified periodicity.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClient3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2">IAudioClient2</a>. <b>IAudioClient3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClient3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient3-getcurrentsharedmodeengineperiod">GetCurrentSharedModeEnginePeriod</a>
</td>
<td align="left" width="63%">
Returns the current format and periodicity of the audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient3-getsharedmodeengineperiod">GetSharedModeEnginePeriod</a>
</td>
<td align="left" width="63%">
Returns the range of periodicities supported by the engine for the specified stream format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient3-initializesharedaudiostream">InitializeSharedAudioStream</a>
</td>
<td align="left" width="63%">
Initializes a shared stream with the specified periodicity.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2">IAudioClient2</a>
 

 

