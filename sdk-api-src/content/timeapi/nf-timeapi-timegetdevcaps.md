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

# timeGetDevCaps function


## -description



        The <b>timeGetDevCaps</b> function queries the timer device to determine its resolution.
      


## -parameters




### -param ptc


            A pointer to a <a href="https://msdn.microsoft.com/64a5c4ba-d340-4abc-8da3-766f3a2d7ec8">TIMECAPS</a> structure. This structure is filled with information about the resolution of the timer device.
          


### -param cbtc

The size, in bytes, of the <a href="https://msdn.microsoft.com/64a5c4ba-d340-4abc-8da3-766f3a2d7ec8">TIMECAPS</a> structure.
          


## -returns



Returns <b>MMSYSERR_NOERROR</b> if successful or an error code otherwise. Possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_ERROR</b></dt>
</dl>
</td>
<td width="60%">
General error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIMERR_NOCANDO</b></dt>
</dl>
</td>
<td width="60%">
The <i>ptc</i> parameter is <b>NULL</b>, or the <i>cbtc</i> parameter is invalid, or some other error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/71680295-7fd3-4a8b-a574-78ea05e1d11d">Multimedia Timer Functions</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>



<a href="https://msdn.microsoft.com/2e5e94fe-8175-417f-8c59-9d5cf052ea89">Timer Resolution</a>
 

 

