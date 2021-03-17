---
UID: NF:devicetopology.IAudioChannelConfig.GetChannelConfig
title: IAudioChannelConfig::GetChannelConfig (devicetopology.h)
description: The GetChannelConfig method gets the current channel-configuration mask from a channel-configuration control.
helpviewer_keywords: ["GetChannelConfig","GetChannelConfig method [Core Audio]","GetChannelConfig method [Core Audio]","IAudioChannelConfig interface","IAudioChannelConfig interface [Core Audio]","GetChannelConfig method","IAudioChannelConfig.GetChannelConfig","IAudioChannelConfig::GetChannelConfig","IAudioChannelConfigGetChannelConfig","coreaudio.iaudiochannelconfig_getchannelconfig","devicetopology/IAudioChannelConfig::GetChannelConfig"]
old-location: coreaudio\iaudiochannelconfig_getchannelconfig.htm
tech.root: CoreAudio
ms.assetid: 91331c34-9805-424b-b2c9-5705a11c594d
ms.date: 12/05/2018
ms.keywords: GetChannelConfig, GetChannelConfig method [Core Audio], GetChannelConfig method [Core Audio],IAudioChannelConfig interface, IAudioChannelConfig interface [Core Audio],GetChannelConfig method, IAudioChannelConfig.GetChannelConfig, IAudioChannelConfig::GetChannelConfig, IAudioChannelConfigGetChannelConfig, coreaudio.iaudiochannelconfig_getchannelconfig, devicetopology/IAudioChannelConfig::GetChannelConfig
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
 - IAudioChannelConfig::GetChannelConfig
 - devicetopology/IAudioChannelConfig::GetChannelConfig
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
 - IAudioChannelConfig.GetChannelConfig
---

# IAudioChannelConfig::GetChannelConfig


## -description

The <b>GetChannelConfig</b> method gets the current channel-configuration mask from a channel-configuration control.

## -parameters

### -param pdwConfig [out]

Pointer to a <b>DWORD</b> variable into which the method writes the current channel-configuration mask value.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pdwConfig</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For information about channel-configuration masks, see the discussion of the <a href="/windows-hardware/drivers/audio/ksproperty-audio-channel-config">KSPROPERTY_AUDIO_CHANNEL_CONFIG</a> property in the Windows DDK documentation.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiochannelconfig">IAudioChannelConfig Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iaudiochannelconfig-setchannelconfig">IAudioChannelConfig::SetChannelConfig</a>