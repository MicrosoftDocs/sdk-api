---
UID: NN:audioclient.IAudioClockAdjustment
title: IAudioClockAdjustment
author: windows-sdk-content
description: The IAudioClockAdjustment interface is used to adjust the sample rate of a stream.
old-location: coreaudio\iaudioclockadjustment.htm
old-project: CoreAudio
ms.assetid: 61d90fd9-6c73-4987-b424-1523f15ab023
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IAudioClockAdjustment, IAudioClockAdjustment interface [Core Audio], IAudioClockAdjustment interface [Core Audio],described, audioclient/IAudioClockAdjustment, coreaudio.iaudioclockadjustment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IAudioClockAdjustment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClockAdjustment interface


## -description


The <b>IAudioClockAdjustment</b> interface is used to adjust the sample rate of a stream. 
		

The client obtains a reference to the <b>IAudioClockAdjustment</b> interface of a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClockAdjustment. Adjusting the sample rate is not supported for exclusive mode streams. 

The <b>IAudioClockAdjustment</b> interface must be obtained from an audio client that is initialized with both the AUDCLNT_STREAMFLAGS_RATEADJUST flag  and the share mode set to AUDCLNT_SHAREMODE_SHARED.
			  If <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">Initialize</a> is called in an exclusive mode with the AUDCLNT_STREAMFLAGS_RATEADJUST flag, <b>Initialize</b> fails with the  AUDCLNT_E_UNSUPPORTED_FORMAT error code.

When releasing an <b>IAudioClockAdjustment</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> that created the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClockAdjustment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioClockAdjustment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClockAdjustment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbb5b525-dc5a-4845-a1fa-ed37281b5c69">SetSampleRate</a>
</td>
<td align="left" width="63%">
Sets the sample rate of a stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7b2267c3-79f5-4ada-a7ce-78dd514f8487">AUDCLNT_STREAMFLAGS_XXX Constants</a>



<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

