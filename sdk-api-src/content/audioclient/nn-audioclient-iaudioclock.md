---
UID: NN:audioclient.IAudioClock
title: IAudioClock (audioclient.h)
author: windows-sdk-content
description: The IAudioClock interface enables a client to monitor a stream's data rate and the current position in the stream.
old-location: coreaudio\iaudioclock.htm
tech.root: CoreAudio
ms.assetid: dbec9468-b555-42a0-a988-dec3a66c9f96
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioClock, IAudioClock interface [Core Audio], IAudioClock interface [Core Audio],described, audioclient/IAudioClock, coreaudio.iaudioclock
ms.topic: interface
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Audioclient.h
api_name:
 - IAudioClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioClock interface


## -description



The <b>IAudioClock</b> interface enables a client to monitor a stream's data rate and the current position in the stream. The client obtains a reference to the <b>IAudioClock</b> interface of a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClock.

When releasing an <b>IAudioClock</b> interface instance, the client must call the interface's Release method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5439a03-9f51-4e51-ab2e-0263de8a3468">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ad17f03-a353-4ac5-9f07-b5dc7c3b530f">GetFrequency</a>
</td>
<td align="left" width="63%">
Gets the device frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2271bd73-8cb6-4048-a16c-f765d0fae6bd">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the current position in the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

