---
UID: NN:audioclient.IAudioClient3
title: IAudioClient3
author: windows-driver-content
description: The IAudioClient3 interface is derived from the IAudioClient2 interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to query for the audio engine's supported periodicities and current periodicity as well as request initialization a shared audio stream with a specified periodicity.
old-location: coreaudio\iaudioclient3.htm
old-project: CoreAudio
ms.assetid: E8EFE682-E1BC-4D0D-A60E-DD257D6E5894
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: IAudioClient3, IAudioClient3 interface [Core Audio], IAudioClient3 interface [Core Audio],described, audioclient/IAudioClient3, coreaudio.iaudioclient3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
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
-	IAudioClient3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient3 interface


## -description


The <b>IAudioClient3</b> interface is derived from the <a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a> interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to query for the audio engine's supported periodicities and current periodicity as well as request initialization a shared audio stream with a specified periodicity.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClient3</b> interface inherits from <a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a>. <b>IAudioClient3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/F91E46F5-5D12-4D53-842B-4495CAA3E09E">GetCurrentSharedModeEnginePeriod</a>
</td>
<td align="left" width="63%">
Returns the current format and periodicity of the audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41ED045F-0C47-40BE-9ECD-6A925E166E6D">GetSharedModeEnginePeriod</a>
</td>
<td align="left" width="63%">
Returns the range of periodicities supported by the engine for the specified stream format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2DB9ECEC-8199-4157-8854-26A21B88E58A">InitializeSharedAudioStream</a>
</td>
<td align="left" width="63%">
Initializes a shared stream with the specified periodicity.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a>
 

 

