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

# IAudioMute::GetMute


## -description



The <b>GetMute</b> method gets the current state (enabled or disabled) of the mute control.




## -parameters




### -param pbMuted [out]

Pointer to a <b>BOOL</b> variable into which the method writes the current state of the mute control. If the state is <b>TRUE</b>, muting is enabled. If <b>FALSE</b>, it is disabled.


## -returns



<table>
<tr>
<th>
                  Return code
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>E_POINTER</td>
<td>Pointer <i>pbMuted</i> is <b>NULL</b>.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/53d49af7-81c3-4e75-ba06-dcee34d84292">IAudioMute Interface</a>
 

 

