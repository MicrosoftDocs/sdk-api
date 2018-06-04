---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAudioClockAdjustment interface


## -description



			The <b>IAudioClockAdjustment</b> interface is used to adjust the sample rate of a stream. 
		

The client obtains a reference to the <b>IAudioClockAdjustment</b> interface of a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClockAdjustment. Adjusting the sample rate is not supported for exclusive mode streams. 

The <b>IAudioClockAdjustment</b> interface must be obtained from an audio client that is initialized with both the AUDCLNT_STREAMFLAGS_RATEADJUST flag  and the share mode set to AUDCLNT_SHAREMODE_SHARED.
			  If <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> is called in an exclusive mode with the AUDCLNT_STREAMFLAGS_RATEADJUST flag, <b>Initialize</b> fails with the  AUDCLNT_E_UNSUPPORTED_FORMAT error code.

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
 

 

