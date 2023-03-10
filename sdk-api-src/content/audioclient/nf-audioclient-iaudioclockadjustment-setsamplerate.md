---
UID: NF:audioclient.IAudioClockAdjustment.SetSampleRate
title: IAudioClockAdjustment::SetSampleRate (audioclient.h)
description: The SetSampleRate method sets the sample rate of a stream.
helpviewer_keywords: ["IAudioClockAdjustment interface [Core Audio]","SetSampleRate method","IAudioClockAdjustment.SetSampleRate","IAudioClockAdjustment::SetSampleRate","SetSampleRate","SetSampleRate method [Core Audio]","SetSampleRate method [Core Audio]","IAudioClockAdjustment interface","audioclient/IAudioClockAdjustment::SetSampleRate","coreaudio.iaudioclockadjustment_setsamplerate"]
old-location: coreaudio\iaudioclockadjustment_setsamplerate.htm
tech.root: CoreAudio
ms.assetid: fbb5b525-dc5a-4845-a1fa-ed37281b5c69
ms.date: 12/05/2018
ms.keywords: IAudioClockAdjustment interface [Core Audio],SetSampleRate method, IAudioClockAdjustment.SetSampleRate, IAudioClockAdjustment::SetSampleRate, SetSampleRate, SetSampleRate method [Core Audio], SetSampleRate method [Core Audio],IAudioClockAdjustment interface, audioclient/IAudioClockAdjustment::SetSampleRate, coreaudio.iaudioclockadjustment_setsamplerate
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAudioClockAdjustment::SetSampleRate
 - audioclient/IAudioClockAdjustment::SetSampleRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClockAdjustment.SetSampleRate
---

# IAudioClockAdjustment::SetSampleRate


## -description

The <b>SetSampleRate</b> method sets the sample rate of a stream.

## -parameters

### -param flSampleRate [in]

The new sample rate in frames per second.

## -returns

If the method succeeds, it returns S_OK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been successfully initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The sample rate is out of the range for the Audio Processing Object.

</td>
</tr>
</table>

## -remarks

This method must not be called from a real-time processing thread.
			
		    

The new sample rate will take effect after the current frame is done processing and will remain in effect until <b>SetSampleRate</b> is called again.
		The audio client must be initialized in shared-mode (AUDCLNT_SHAREMODE_SHARED), otherwise <b>SetSampleRate</b> fails.

## -see-also

<a href="/windows/desktop/CoreAudio/audclnt-streamflags-xxx-constants">AUDCLNT_STREAMFLAGS_XXX Constants</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment">IAudioClockAdjustment</a>