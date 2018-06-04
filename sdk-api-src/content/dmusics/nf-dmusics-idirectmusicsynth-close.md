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

# IDirectMusicSynth::Close


## -description


The <code>Close</code> method closes a DirectMusic "port", which is a DirectMusic term for a device that sends or receives music data.


## -parameters






#### - None


## -returns



<code>Close</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_ALREADYCLOSED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the port was not open.

</td>
</tr>
</table>
 




## -remarks



This method closes a DirectMusic "port" that was previously opened by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536539">IDirectMusicSynth::Open</a>.

When the DirectMusic "port" closes, it automatically releases all instruments and waves that were previously downloaded to the port. However, a good practice for applications is to explicitly free these objects before closing the port.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536539">IDirectMusicSynth::Open</a>
 

 

