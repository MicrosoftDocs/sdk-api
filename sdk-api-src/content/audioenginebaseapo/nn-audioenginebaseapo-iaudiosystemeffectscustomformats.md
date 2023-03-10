---
UID: NN:audioenginebaseapo.IAudioSystemEffectsCustomFormats
title: IAudioSystemEffectsCustomFormats (audioenginebaseapo.h)
description: The IAudioSystemEffectsCustomFormats interface is supported in Windows Vista and later versions of Windows.
helpviewer_keywords: ["IAudioSystemEffectsCustomFormats","IAudioSystemEffectsCustomFormats interface [Audio Devices]","IAudioSystemEffectsCustomFormats interface [Audio Devices]","described","audio.iaudiosystemeffectscustomformats","audio_syseffects_r_c8bb1589-9952-4e31-8153-653c3dd0f174.xml","audioenginebaseapo/IAudioSystemEffectsCustomFormats"]
old-location: audio\iaudiosystemeffectscustomformats.htm
tech.root: audio
ms.assetid: 29b758c0-5bbe-489c-9950-bc92a185fbaf
ms.date: 12/05/2018
ms.keywords: IAudioSystemEffectsCustomFormats, IAudioSystemEffectsCustomFormats interface [Audio Devices], IAudioSystemEffectsCustomFormats interface [Audio Devices],described, audio.iaudiosystemeffectscustomformats, audio_syseffects_r_c8bb1589-9952-4e31-8153-653c3dd0f174.xml, audioenginebaseapo/IAudioSystemEffectsCustomFormats
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioSystemEffectsCustomFormats
 - audioenginebaseapo/IAudioSystemEffectsCustomFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioSystemEffectsCustomFormats
---

# IAudioSystemEffectsCustomFormats interface


## -description

The <code>IAudioSystemEffectsCustomFormats</code> interface is supported in Windows Vista and later versions of Windows. When you develop an audio processing object (APO) to drive an audio adapter with  an atypical format, the APO must support the <code>IAudioSystemEffectsCustomFormats</code> interface.

The Windows operating system can instantiate your APO outside the audio engine and use the <code>IAudioSystemEffectsCustomFormats</code> interface to retrieve information about the atypical format. The associated user interface displays the data that is retrieved.
<div class="alert"><b>Important</b>  Although the <code>IAudioSystemEffectsCustomFormats</code> interface  continues to be supported in Windows, note that the type of APO to which you can apply this interface depends on the version of Windows you are targeting. The following table provides more information:</div><div> </div><table>
<tr>
<th>Target OS</th>
<th>Target APO type</th>
</tr>
<tr>
<td>Windows Vista</td>
<td>Global effects (GFX)</td>
</tr>
<tr>
<td>Windows 7</td>
<td>Global effects (GFX)</td>
</tr>
<tr>
<td>Windows 8</td>
<td>Global effects (GFX)</td>
</tr>
<tr>
<td>Windows 8.1</td>
<td>Endpoint effects (EFX)</td>
</tr>
</table> 

The <code>IAudioSystemEffectsCustomFormats</code> interface inherits from <b>IUnknown</b> and also supports the following methods:
<dl>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformat">IAudioSystemEffectsCustomFormats::GetFormat</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformatcount">IAudioSystemEffectsCustomFormats::GetFormatCount</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformatrepresentation">IAudioSystemEffectsCustomFormats::GetFormatRepresentation</a>


</dd>
</dl>