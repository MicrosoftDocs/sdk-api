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

# IMSVidStreamBufferSourceEvent2::RateChange


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>RateChange</b> method is called when the playback rate changes.


## -parameters




### -param qwNewRate [in]

Specifies the new playback rate.


### -param qwOldRate [in]

Specifies the previous playback rate.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
</table>
 




## -remarks



For both parameters, 1.0 represents normal speed. Fractional values are allowed. For example, 0.2 would represent a rate that is slower than normal playback and 1.7 would represent a rate that is faster than normal playback.




## -see-also




<a href="https://msdn.microsoft.com/d601efcf-d15a-4b9a-bad8-f09de80500c6">IMSVidStreamBufferSourceEvent2 Interface</a>
 

 

