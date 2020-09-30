---
UID: NN:wmprealestate.IWMPAudioRenderConfig
title: IWMPAudioRenderConfig (wmprealestate.h)
description: The IWMPAudioRenderConfig interface provides methods for setting and retrieving the audio output device used by the Windows Media Player ActiveX control.
helpviewer_keywords: ["IWMPAudioRenderConfig","IWMPAudioRenderConfig interface [Windows Media Player]","IWMPAudioRenderConfig interface [Windows Media Player]","described","wmp.iwmpaudiorenderconfig","wmprealestate/IWMPAudioRenderConfig"]
old-location: wmp\iwmpaudiorenderconfig.htm
tech.root: WMP
ms.assetid: 743dae18-985a-405a-8025-ead54e06a4ea
ms.date: 12/05/2018
ms.keywords: IWMPAudioRenderConfig, IWMPAudioRenderConfig interface [Windows Media Player], IWMPAudioRenderConfig interface [Windows Media Player],described, wmp.iwmpaudiorenderconfig, wmprealestate/IWMPAudioRenderConfig
req.header: wmprealestate.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPAudioRenderConfig
 - wmprealestate/IWMPAudioRenderConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmprealestate.h
api_name:
 - IWMPAudioRenderConfig
 - IWMPAudioRenderConfig.get_audioOutputDevice
 - IWMPAudioRenderConfig.put_audioOutputDevice
---

# IWMPAudioRenderConfig interface


## -description

The <b>IWMPAudioRenderConfig</b> interface provides methods for setting and retrieving the audio output device used by the Windows Media Player ActiveX control.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPAudioRenderConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPAudioRenderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPAudioRenderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">get_audioOutputDevice</td>
<td align="left" width="63%">
Retrieves the current audio output device used by the Windows Media Player ActiveX control.   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">put_audioOutputDevice</td>
<td align="left" width="63%">
Sets the current audio output device for the Windows Media Player ActiveX control.  

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/WMP/interfaces">Interfaces</a>