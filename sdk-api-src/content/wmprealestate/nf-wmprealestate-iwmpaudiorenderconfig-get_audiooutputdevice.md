---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

