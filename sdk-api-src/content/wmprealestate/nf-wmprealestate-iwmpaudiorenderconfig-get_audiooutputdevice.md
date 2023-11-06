---
UID: NF:wmprealestate.IWMPAudioRenderConfig.get_audioOutputDevice
title: IWMPAudioRenderConfig::get_audioOutputDevice (wmprealestate.h)
description: The get_audioOutputDevice method retrieves the current audio output device used by the Windows Media Player ActiveX control.
helpviewer_keywords: ["IWMPAudioRenderConfig interface [Windows Media Player]","get_audioOutputDevice method","IWMPAudioRenderConfig.get_audioOutputDevice","IWMPAudioRenderConfig::get_audioOutputDevice","get_audioOutputDevice","get_audioOutputDevice method [Windows Media Player]","get_audioOutputDevice method [Windows Media Player]","IWMPAudioRenderConfig interface","wmp.iwmpaudiorenderconfig_get_audiooutputdevice","wmprealestate/IWMPAudioRenderConfig::get_audioOutputDevice"]
old-location: wmp\iwmpaudiorenderconfig_get_audiooutputdevice.htm
tech.root: WMP
ms.assetid: a6ad388e-0fb8-4188-853c-9eba67e0848e
ms.date: 4/26/2023
ms.keywords: IWMPAudioRenderConfig interface [Windows Media Player],get_audioOutputDevice method, IWMPAudioRenderConfig.get_audioOutputDevice, IWMPAudioRenderConfig::get_audioOutputDevice, get_audioOutputDevice, get_audioOutputDevice method [Windows Media Player], get_audioOutputDevice method [Windows Media Player],IWMPAudioRenderConfig interface, wmp.iwmpaudiorenderconfig_get_audiooutputdevice, wmprealestate/IWMPAudioRenderConfig::get_audioOutputDevice
req.header: wmprealestate.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 12
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPAudioRenderConfig::get_audioOutputDevice
 - wmprealestate/IWMPAudioRenderConfig::get_audioOutputDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPAudioRenderConfig.get_audioOutputDevice
---

# IWMPAudioRenderConfig::get_audioOutputDevice


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_audioOutputDevice</b> method retrieves the current audio output device used by the Windows Media Player ActiveX control.

## -parameters

### -param pbstrOutputDevice

An MMDeviceAPI device ID that represents the currently configured audio output device.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

If no default audio device is configured, this method retrieves an empty <b>BSTR</b>.  If the ActiveX control is hosted in the Windows Media Player, and the Player has configured an output device, this method retrieves the output device configured by the Player.

If this method retrieves an empty string, the Windows Media Player ActiveX control will render using the default audio rendering device.

## -see-also

<a href="/windows/desktop/CoreAudio/mmdevice-api">About MMDevice API</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig">IWMPAudioRenderConfig</a>