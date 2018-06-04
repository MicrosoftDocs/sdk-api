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

# IMixerOCXNotify::OnDataChange


## -description



The <code>OnDataChange</code> method notifies the client when the video rectangle's aspect ratio or size, or the display palette, has changed.




## -parameters




### -param ulDataFlags [in]

Flag indicating which set of data has changed. The following flags are defined.

<table>
<tr>
<th>
                  Flags
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MIXER_DATA_ASPECT_RATIO (0x00000001)</td>
<td>Picture aspect ratio.</td>
</tr>
<tr>
<td>MIXER_DATA_NATIVE_SIZE (0x00000002)</td>
<td>The video stream's native size changed.</td>
</tr>
<tr>
<td>MIXER_DATA_PALETTE (0x00000004)</td>
<td>The video palette changed.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/b80d720d-921d-4d24-a168-49944cfcc411">IMixerOCX Interface</a>



<a href="https://msdn.microsoft.com/b73416c0-2312-4164-8a6d-f8776dc1447f">IMixerOCXNotify Interface</a>
 

 

