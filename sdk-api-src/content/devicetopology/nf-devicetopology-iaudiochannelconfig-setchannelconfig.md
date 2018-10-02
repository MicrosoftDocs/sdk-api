---
UID: NF:devicetopology.IAudioChannelConfig.SetChannelConfig
title: IAudioChannelConfig::SetChannelConfig
author: windows-sdk-content
description: The SetChannelConfig method sets the channel-configuration mask in a channel-configuration control.
old-location: coreaudio\iaudiochannelconfig_setchannelconfig.htm
tech.root: CoreAudio
ms.assetid: a63b92ab-8abf-4582-b408-6c3e94a6bd3c
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IAudioChannelConfig interface [Core Audio],SetChannelConfig method, IAudioChannelConfig.SetChannelConfig, IAudioChannelConfig::SetChannelConfig, IAudioChannelConfigSetChannelConfig, SetChannelConfig, SetChannelConfig method [Core Audio], SetChannelConfig method [Core Audio],IAudioChannelConfig interface, coreaudio.iaudiochannelconfig_setchannelconfig, devicetopology/IAudioChannelConfig::SetChannelConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: devicetopology.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioChannelConfig.SetChannelConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioChannelConfig::SetChannelConfig


## -description



The <b>SetChannelConfig</b> method sets the channel-configuration mask in a channel-configuration control.




## -parameters




### -param dwConfig [in]

The channel-configuration mask.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a2f32cb9-3c8b-4b44-96a2-dd70afcca71a">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetChannelConfig</b> call changes the state of the channel-configuration control, all clients that have registered <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



For information about channel-configuration masks, see the discussion of the <a href="https://msdn.microsoft.com/5ce9bf4a-c84e-4d7e-8e75-896c88ec1a72">KSPROPERTY_AUDIO_CHANNEL_CONFIG</a> property in the Windows DDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/b8e54e9e-a6eb-46e6-a71c-ff498c7e8f47">IAudioChannelConfig Interface</a>



<a href="https://msdn.microsoft.com/91331c34-9805-424b-b2c9-5705a11c594d">IAudioChannelConfig::GetChannelConfig</a>
 

 

