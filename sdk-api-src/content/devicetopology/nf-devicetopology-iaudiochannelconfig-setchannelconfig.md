---
UID: NF:devicetopology.IAudioChannelConfig.SetChannelConfig
title: IAudioChannelConfig::SetChannelConfig (devicetopology.h)
description: The SetChannelConfig method sets the channel-configuration mask in a channel-configuration control.
helpviewer_keywords: ["IAudioChannelConfig interface [Core Audio]","SetChannelConfig method","IAudioChannelConfig.SetChannelConfig","IAudioChannelConfig::SetChannelConfig","IAudioChannelConfigSetChannelConfig","SetChannelConfig","SetChannelConfig method [Core Audio]","SetChannelConfig method [Core Audio]","IAudioChannelConfig interface","coreaudio.iaudiochannelconfig_setchannelconfig","devicetopology/IAudioChannelConfig::SetChannelConfig"]
old-location: coreaudio\iaudiochannelconfig_setchannelconfig.htm
tech.root: CoreAudio
ms.assetid: a63b92ab-8abf-4582-b408-6c3e94a6bd3c
ms.date: 12/05/2018
ms.keywords: IAudioChannelConfig interface [Core Audio],SetChannelConfig method, IAudioChannelConfig.SetChannelConfig, IAudioChannelConfig::SetChannelConfig, IAudioChannelConfigSetChannelConfig, SetChannelConfig, SetChannelConfig method [Core Audio], SetChannelConfig method [Core Audio],IAudioChannelConfig interface, coreaudio.iaudiochannelconfig_setchannelconfig, devicetopology/IAudioChannelConfig::SetChannelConfig
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioChannelConfig::SetChannelConfig
 - devicetopology/IAudioChannelConfig::SetChannelConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioChannelConfig.SetChannelConfig
---

# IAudioChannelConfig::SetChannelConfig


## -description

The <b>SetChannelConfig</b> method sets the channel-configuration mask in a channel-configuration control.

## -parameters

### -param dwConfig [in]

The channel-configuration mask.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetChannelConfig</b> call changes the state of the channel-configuration control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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

For information about channel-configuration masks, see the discussion of the <a href="/windows-hardware/drivers/audio/ksproperty-audio-channel-config">KSPROPERTY_AUDIO_CHANNEL_CONFIG</a> property in the Windows DDK documentation.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiochannelconfig-getchannelconfig">IAudioChannelConfig::GetChannelConfig</a>