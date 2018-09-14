---
UID: NF:wmprealestate.IWMPAudioRenderConfig.put_audioOutputDevice
title: IWMPAudioRenderConfig::put_audioOutputDevice
author: windows-sdk-content
description: The put_audioOutputDevice sets the current audio output device for the Windows Media Player ActiveX control.
old-location: wmp\iwmpaudiorenderconfig_put_audiooutputdevice.htm
tech.root: WMP
ms.assetid: c8e88b36-fb40-4550-bef0-16d92f2bdd2a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPAudioRenderConfig interface [Windows Media Player],put_audioOutputDevice method, IWMPAudioRenderConfig.put_audioOutputDevice, IWMPAudioRenderConfig::put_audioOutputDevice, put_audioOutputDevice, put_audioOutputDevice method [Windows Media Player], put_audioOutputDevice method [Windows Media Player],IWMPAudioRenderConfig interface, wmp.iwmpaudiorenderconfig_put_audiooutputdevice, wmprealestate/IWMPAudioRenderConfig::put_audioOutputDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPAudioRenderConfig.put_audioOutputDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPAudioRenderConfig::put_audioOutputDevice


## -description


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




<a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">About MMDevice API</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/743dae18-985a-405a-8025-ead54e06a4ea">IWMPAudioRenderConfig</a>
 

 

