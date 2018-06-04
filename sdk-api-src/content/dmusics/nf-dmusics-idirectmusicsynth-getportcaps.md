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

# IDirectMusicSynth::GetPortCaps


## -description


The <code>GetPortCaps</code> method retrieves the capabilities of a DirectMusic "port", which is a DirectMusic term for a device that sends or receives music data.


## -parameters




### -param pCaps

Pointer to a DMUS_PORTCAPS structure (described in the Microsoft Windows SDK documentation). The method writes the capabilities of the DirectMusic "port" into this structure.


## -returns



<code>GetPortCaps</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates a bad <i>pCaps</i> pointer.

</td>
</tr>
</table>
 




## -remarks



When an application enumerates the available DirectMusic "ports" with a call to <b>IDirectMusic::EnumPort</b> (described in the Windows SDK documentation), DirectMusic calls each registered device's <code>GetPortCaps</code> method.

This means that the additional overhead of creating and initializing the synthesizer occurs with this call. It is a good idea to keep the overhead of simply creating a synthesizer to a minimum, because there is a chance that it is being created only so that its capabilities can be obtained, and then it will be released.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Windows SDK documentation.



