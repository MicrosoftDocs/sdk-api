---
UID: NN:spatialaudioclient.IAudioFormatEnumerator
title: IAudioFormatEnumerator
author: windows-sdk-content
description: Provides a list of supported audio formats. The most preferred format is first in the list. Get a reference to this interface by calling ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator.
old-location: coreaudio\iaudioformatenumerator.htm
old-project: CoreAudio
ms.assetid: 50434617-E70E-4931-B98E-61650E9DEA7E
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioFormatEnumerator, IAudioFormatEnumerator interface [Core Audio], IAudioFormatEnumerator interface [Core Audio],described, coreaudio.iaudioformatenumerator, spatialaudioclient/IAudioFormatEnumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudioclient.h
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
req.typenames: AudioObjectType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	spatialaudioclient.h
api_name:
-	IAudioFormatEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAudioFormatEnumerator interface


## -description


Provides a list of supported audio formats. The most preferred format is first in the list. Get a reference to this interface by calling <a href="https://msdn.microsoft.com/CB152D8C-DE3A-4224-A6CC-DF1BFF1A3ABA">ISpatialAudioClient::GetSupportedAudioObjectFormatEnumerator</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioFormatEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioFormatEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioFormatEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of supported audio formats in the list

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9949F688-51D1-418B-947D-2607C90CA4E4">GetFormat</a>
</td>
<td align="left" width="63%">
Gets the format with the specified index in the list. The formats are listed in order of importance. The most preferable format is first in the list.

</td>
</tr>
</table> 

