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

# IAMTuner::SignalPresent


## -description



The <code>SignalPresent</code> method retrieves the strength of the signal on a given channel.




## -parameters




### -param plSignalStrength [out]

Pointer to a variable that receives a value indicating whether a signal is present on the current channel. Can be one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>AMTUNER_HASNOSIGNALSTRENGTH</td>
<td>-1</td>
</tr>
<tr>
<td>AMTUNER_NOSIGNAL</td>
<td>0</td>
</tr>
<tr>
<td>AMTUNER_SIGNALPRESENT</td>
<td>1</td>
</tr>
</table>
 

A value of AMTUNER_HASNOSIGNALSTRENGTH means the signal strength cannot be determined at this time.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

