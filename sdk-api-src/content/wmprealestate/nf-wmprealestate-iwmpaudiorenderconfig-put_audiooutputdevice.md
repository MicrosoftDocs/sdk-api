---
UID: NF:wmprealestate.IWMPAudioRenderConfig.put_audioOutputDevice
title: IWMPAudioRenderConfig::put_audioOutputDevice (wmprealestate.h)
description: The put_audioOutputDevice sets the current audio output device for the Windows Media Player ActiveX control.
helpviewer_keywords: ["IWMPAudioRenderConfig interface [Windows Media Player]","put_audioOutputDevice method","IWMPAudioRenderConfig.put_audioOutputDevice","IWMPAudioRenderConfig::put_audioOutputDevice","put_audioOutputDevice","put_audioOutputDevice method [Windows Media Player]","put_audioOutputDevice method [Windows Media Player]","IWMPAudioRenderConfig interface","wmp.iwmpaudiorenderconfig_put_audiooutputdevice","wmprealestate/IWMPAudioRenderConfig::put_audioOutputDevice"]
old-location: wmp\iwmpaudiorenderconfig_put_audiooutputdevice.htm
tech.root: WMP
ms.assetid: c8e88b36-fb40-4550-bef0-16d92f2bdd2a
ms.date: 4/26/2023
ms.keywords: IWMPAudioRenderConfig interface [Windows Media Player],put_audioOutputDevice method, IWMPAudioRenderConfig.put_audioOutputDevice, IWMPAudioRenderConfig::put_audioOutputDevice, put_audioOutputDevice, put_audioOutputDevice method [Windows Media Player], put_audioOutputDevice method [Windows Media Player],IWMPAudioRenderConfig interface, wmp.iwmpaudiorenderconfig_put_audiooutputdevice, wmprealestate/IWMPAudioRenderConfig::put_audioOutputDevice
req.header: wmprealestate.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 12.
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
 - IWMPAudioRenderConfig::put_audioOutputDevice
 - wmprealestate/IWMPAudioRenderConfig::put_audioOutputDevice
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
 - IWMPAudioRenderConfig.put_audioOutputDevice
---

# IWMPAudioRenderConfig::put_audioOutputDevice


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_audioOutputDevice</b> sets the current audio output device for the Windows Media Player ActiveX control.

## -parameters

### -param bstrOutputDevice

An MMDeviceAPI device ID that represents the device. If you pass <b>NULL</b> or an empty <b>BSTR</b> to this method, the Windows Media Player ActiveX control reverts to the default audio output device.

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

This method validates that the endpoint specified in <i>bstrOutputDevice</i> is a valid MMDeviceAPI device identifier string for an audio output endpoint. If it is not a valid identifier, the method fails.  This method does not check to ensure that the specified endpoint is active.

## -see-also

<a href="/windows/desktop/CoreAudio/mmdevice-api">About MMDevice API</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig">IWMPAudioRenderConfig</a>