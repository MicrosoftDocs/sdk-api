---
UID: NF:wmprealestate.IWMPAudioRenderConfig.get_audioOutputDevice
title: IWMPAudioRenderConfig::get_audioOutputDevice
author: windows-sdk-content
description: The get_audioOutputDevice method retrieves the current audio output device used by the Windows Media Player ActiveX control.
old-location: wmp\iwmpaudiorenderconfig_get_audiooutputdevice.htm
tech.root: WMP
ms.assetid: a6ad388e-0fb8-4188-853c-9eba67e0848e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPAudioRenderConfig interface [Windows Media Player],get_audioOutputDevice method, IWMPAudioRenderConfig.get_audioOutputDevice, IWMPAudioRenderConfig::get_audioOutputDevice, get_audioOutputDevice, get_audioOutputDevice method [Windows Media Player], get_audioOutputDevice method [Windows Media Player],IWMPAudioRenderConfig interface, wmp.iwmpaudiorenderconfig_get_audiooutputdevice, wmprealestate/IWMPAudioRenderConfig::get_audioOutputDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPAudioRenderConfig.get_audioOutputDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmprealestate.h
: 
- IWMPAudioRenderConfig.get_audioOutputDevice
: 
---

# IWMPAudioRenderConfig::get_audioOutputDevice


## -description


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




<a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">About MMDevice API</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/743dae18-985a-405a-8025-ead54e06a4ea">IWMPAudioRenderConfig</a>
 

 

