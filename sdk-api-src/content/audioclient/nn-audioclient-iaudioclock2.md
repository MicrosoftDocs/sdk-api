---
UID: NN:audioclient.IAudioClock2
title: IAudioClock2 (audioclient.h)
author: windows-sdk-content
description: The IAudioClock2 interface is used to get the current device position.
old-location: coreaudio\iaudioclock2.htm
tech.root: CoreAudio
ms.assetid: 4820c93a-a5d8-4ab9-aefc-9377fc76e745
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioClock2, IAudioClock2 interface [Core Audio], IAudioClock2 interface [Core Audio],described, audioclient/IAudioClock2, coreaudio.iaudioclock2
ms.topic: interface
f1_keywords: 
 - "audioclient/IAudioClock2"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClock2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioClock2 interface


## -description


The <b>IAudioClock2</b> interface is used to get the current device position.
		

To get a reference to the <b>IAudioClock2</b> interface, the application must call <b>IAudioClock::QueryInterface</b> to request the interface pointer from the stream object's  <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock</a> interface.
	

The client obtains a reference to the <b>IAudioClock</b> interface of a stream object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClock.
	

When releasing an <b>IAudioClock2</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> that created the object.
	


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClock2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioClock2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclock2-getdeviceposition">GetDevicePosition</a>
</td>
<td align="left" width="63%">
Gets the current device position, in frames, directly from  the hardware.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock</a>
 

 

