---
UID: NN:audioclient.IAudioClock2
title: IAudioClock2
author: windows-driver-content
description: The IAudioClock2 interface is used to get the current device position.
old-location: coreaudio\iaudioclock2.htm
old-project: CoreAudio
ms.assetid: 4820c93a-a5d8-4ab9-aefc-9377fc76e745
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: IAudioClock2, IAudioClock2 interface [Core Audio], IAudioClock2 interface [Core Audio], described, audioclient/IAudioClock2, coreaudio.iaudioclock2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	audioclient.h
api_name:
-	IAudioClock2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClock2 interface


## -description



		  	The <b>IAudioClock2</b> interface is used to get the current device position.
		


		To get a reference to the <b>IAudioClock2</b> interface, the application must call <b>IAudioClock::QueryInterface</b> to request the interface pointer from the stream object's  <a href="https://msdn.microsoft.com/dbec9468-b555-42a0-a988-dec3a66c9f96">IAudioClock</a> interface.
	


		The client obtains a reference to the <b>IAudioClock</b> interface of a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClock.
	


		When releasing an <b>IAudioClock2</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> that created the object.
	


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClock2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioClock2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClock2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2767056d-59dc-4f6e-b0f7-e37b3fed9581">GetDevicePosition</a>
</td>
<td align="left" width="63%">
Gets the current device position, in frames, directly from  the hardware.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/dbec9468-b555-42a0-a988-dec3a66c9f96">IAudioClock</a>
 

 

