---
UID: NN:wmprealestate.IWMPAudioRenderConfig
title: IWMPAudioRenderConfig
author: windows-driver-content
description: The IWMPAudioRenderConfig interface provides methods for setting and retrieving the audio output device used by the Windows Media Player ActiveX control.
old-location: wmp\iwmpaudiorenderconfig.htm
old-project: WMP
ms.assetid: 743dae18-985a-405a-8025-ead54e06a4ea
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPAudioRenderConfig, IWMPAudioRenderConfig interface [Windows Media Player], IWMPAudioRenderConfig interface [Windows Media Player], described, wmp.iwmpaudiorenderconfig, wmprealestate/IWMPAudioRenderConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmprealestate.h
api_name:
-	IWMPAudioRenderConfig
-	IWMPAudioRenderConfig.get_audioOutputDevice
-	IWMPAudioRenderConfig.put_audioOutputDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPAudioRenderConfig interface


## -description


The <b>IWMPAudioRenderConfig</b> interface provides methods for setting and retrieving the audio output device used by the Windows Media Player ActiveX control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPAudioRenderConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPAudioRenderConfig</b> also has these types of members:
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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

