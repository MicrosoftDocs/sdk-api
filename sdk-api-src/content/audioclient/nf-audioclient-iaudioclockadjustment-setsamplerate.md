---
UID: NF:audioclient.IAudioClockAdjustment.SetSampleRate
title: IAudioClockAdjustment::SetSampleRate
author: windows-sdk-content
description: The SetSampleRate method sets the sample rate of a stream.
old-location: coreaudio\iaudioclockadjustment_setsamplerate.htm
old-project: CoreAudio
ms.assetid: fbb5b525-dc5a-4845-a1fa-ed37281b5c69
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioClockAdjustment interface [Core Audio],SetSampleRate method, IAudioClockAdjustment.SetSampleRate, IAudioClockAdjustment::SetSampleRate, SetSampleRate, SetSampleRate method [Core Audio], SetSampleRate method [Core Audio],IAudioClockAdjustment interface, audioclient/IAudioClockAdjustment::SetSampleRate, coreaudio.iaudioclockadjustment_setsamplerate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioclient.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClockAdjustment.SetSampleRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/7b2267c3-79f5-4ada-a7ce-78dd514f8487">AUDCLNT_STREAMFLAGS_XXX Constants</a>



<a href="https://msdn.microsoft.com/61d90fd9-6c73-4987-b424-1523f15ab023">IAudioClockAdjustment</a>
 

 

