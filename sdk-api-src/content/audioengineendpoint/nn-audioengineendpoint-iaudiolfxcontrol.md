---
UID: NN:audioengineendpoint.IAudioLfxControl
title: IAudioLfxControl
author: windows-sdk-content
description: The IAudioLfxControl interface allows the client to apply or remove local effects from the offloaded audio stream.
old-location: coreaudio\iaudiolfxcontrol.htm
old-project: CoreAudio
ms.assetid: E4290AE9-7F2E-4D0B-BEAF-F01D95B3E03D
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioLfxControl, IAudioLfxControl interface [Core Audio], IAudioLfxControl interface [Core Audio],described, audioengineendpoint/IAudioLfxControl, coreaudio.iaudiolfxcontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: audioengineendpoint.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioLfxControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioLfxControl interface


## -description


The <b>IAudioLfxControl</b> interface allows the client to apply or remove local effects from the offloaded audio stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioLfxControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioLfxControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioLfxControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33426EAC-13E6-4AF2-9D01-7C3057EB8104">GetLocalEffectsState</a>
</td>
<td align="left" width="63%">
Retrieves the local effects state that is currently applied to the offloaded audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F89C2610-BC71-4309-BCDA-5529B16A3FA7">SetLocalEffectsState</a>
</td>
<td align="left" width="63%">
Sets the local effects state that is applied to the offloaded audio stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

