---
UID: NN:mfidl.IMFAudioPolicy
title: IMFAudioPolicy
author: windows-sdk-content
description: Configures the audio session that is associated with the streaming audio renderer (SAR).
old-location: mf\imfaudiopolicy.htm
tech.root: medfound
ms.assetid: fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFAudioPolicy, IMFAudioPolicy interface [Media Foundation], IMFAudioPolicy interface [Media Foundation],described, fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a, mf.imfaudiopolicy, mfidl/IMFAudioPolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAudioPolicy interface


## -description


Configures the audio session that is associated with the streaming audio renderer (SAR). Use this interface to change how the audio session appears in the Windows volume control.

The SAR exposes this interface as a service. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier MR_AUDIO_POLICY_SERVICE. You can call <b>GetService</b> directly on the SAR or call it on the Media Session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAudioPolicy</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFAudioPolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAudioPolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7826b4a1-5887-46a5-b312-91159596ccf5">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/725892fd-4af6-483d-bb5c-87051fa45ec4">GetGroupingParam</a>
</td>
<td align="left" width="63%">
Retrieves the group of sessions to which this audio session belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2114f15-4357-4b5a-b384-695165d887de">GetIconPath</a>
</td>
<td align="left" width="63%">
Retrieves the icon resource for the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cd48400-8d12-4a6b-95fd-bf6ae7700cb8">SetDisplayName</a>
</td>
<td align="left" width="63%">
Sets the display name of the audio session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c024208-f13f-4fd1-b5a8-b881af226670">SetGroupingParam</a>
</td>
<td align="left" width="63%">
Assigns the audio session to a group of sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/098ad6ae-b1fe-4e74-b494-572770906b14">SetIconPath</a>
</td>
<td align="left" width="63%">
Sets the icon resource for the audio session.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

