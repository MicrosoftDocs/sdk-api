---
UID: NN:audioengineendpoint.IAudioLfxControl
title: IAudioLfxControl (audioengineendpoint.h)
description: The IAudioLfxControl interface allows the client to apply or remove local effects from the offloaded audio stream.
helpviewer_keywords: ["IAudioLfxControl","IAudioLfxControl interface [Core Audio]","IAudioLfxControl interface [Core Audio]","described","audioengineendpoint/IAudioLfxControl","coreaudio.iaudiolfxcontrol"]
old-location: coreaudio\iaudiolfxcontrol.htm
tech.root: CoreAudio
ms.assetid: E4290AE9-7F2E-4D0B-BEAF-F01D95B3E03D
ms.date: 12/05/2018
ms.keywords: IAudioLfxControl, IAudioLfxControl interface [Core Audio], IAudioLfxControl interface [Core Audio],described, audioengineendpoint/IAudioLfxControl, coreaudio.iaudiolfxcontrol
req.header: audioengineendpoint.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioLfxControl
 - audioengineendpoint/IAudioLfxControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioLfxControl
---

# IAudioLfxControl interface


## -description

The <b>IAudioLfxControl</b> interface allows the client to apply or remove local effects from the offloaded audio stream.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioLfxControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioLfxControl</b> also has these types of members:
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
<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiolfxcontrol-getlocaleffectsstate">GetLocalEffectsState</a>
</td>
<td align="left" width="63%">
Retrieves the local effects state that is currently applied to the offloaded audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiolfxcontrol-setlocaleffectsstate">SetLocalEffectsState</a>
</td>
<td align="left" width="63%">
Sets the local effects state that is applied to the offloaded audio stream.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>