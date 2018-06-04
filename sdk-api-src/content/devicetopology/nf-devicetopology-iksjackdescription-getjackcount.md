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

# IKsJackDescription::GetJackCount


## -description



The <b>GetJackCount</b> method gets the number of jacks required to connect to an audio endpoint device.




## -parameters




### -param pcJacks [out]

Pointer to a <b>UINT</b> variable into which the method writes the number of jacks associated with the connector.


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
Pointer <i>pcJacks</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



An audio endpoint device that plays or records a stream that contains multiple channels might require a connection with more than one jack (physical connector).

For example, a set of surround speakers that plays a 6-channel audio stream might require three stereo jacks. In this example, the first jack transmits the channels for the front-left and front-right speakers, the second jack transmits the channels for the front-center and low-frequency-effects (subwoofer) speakers, and the third jack transmits the channels for the side-left and side-right speakers.

After calling this method to retrieve the jack count, call the <a href="https://msdn.microsoft.com/84278805-3b6d-4fae-8770-f9932b0e0fab">IKsJackDescription::GetJackDescription</a> method once for each jack to obtain a description of the jack.




## -see-also




<a href="https://msdn.microsoft.com/0ca9e719-7179-4302-99ff-df137141f58f">IKsJackDescription Interface</a>



<a href="https://msdn.microsoft.com/84278805-3b6d-4fae-8770-f9932b0e0fab">IKsJackDescription::GetJackDescription</a>
 

 

