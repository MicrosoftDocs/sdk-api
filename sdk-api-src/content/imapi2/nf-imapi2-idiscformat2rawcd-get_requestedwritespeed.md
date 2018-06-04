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

# IDiscFormat2RawCD::get_RequestedWriteSpeed


## -description


Retrieves the requested write speed.


## -parameters




### -param value [out]

Requested write speed measured in disc sectors per second.

A value of 0xFFFFFFFF (-1) requests that the write occurs using the fastest supported speed for the media.  


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



This is the value specified in the most recent call to the <a href="https://msdn.microsoft.com/93021007-6ed8-4322-93bb-c52796a4ab66">IDiscFormat2RawCD::SetWriteSpeed</a> method.




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/93021007-6ed8-4322-93bb-c52796a4ab66">IDiscFormat2RawCD::SetWriteSpeed</a>



<a href="https://msdn.microsoft.com/f369f719-7db6-4a79-a5fa-d174bf12acbc">IDiscFormat2RawCD::get_CurrentWriteSpeed</a>



<a href="https://msdn.microsoft.com/7ebcc42f-d864-407f-a1a6-d4811ca8221c">IDiscFormat2RawCD::get_SupportedWriteSpeeds</a>
 

 

