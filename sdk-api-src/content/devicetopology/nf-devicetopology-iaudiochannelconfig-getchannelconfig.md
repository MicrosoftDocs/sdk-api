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



For information about channel-configuration masks, see the discussion of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537250">KSPROPERTY_AUDIO_CHANNEL_CONFIG</a> property in the Windows DDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/b8e54e9e-a6eb-46e6-a71c-ff498c7e8f47">IAudioChannelConfig Interface</a>



<a href="https://msdn.microsoft.com/a63b92ab-8abf-4582-b408-6c3e94a6bd3c">IAudioChannelConfig::SetChannelConfig</a>
 

 

