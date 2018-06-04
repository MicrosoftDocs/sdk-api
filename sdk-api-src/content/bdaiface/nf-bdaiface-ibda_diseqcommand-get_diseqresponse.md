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

# IBDA_DiseqCommand::get_DiseqResponse


## -description


Gets the driver's response to a Digital Satellite Equipment Control (DiSEqC) command.


## -parameters




### -param ulRequestId [in]

The identifier of the command. The application assigns this value when it calls <a href="https://msdn.microsoft.com/5ee77311-0b1d-43b1-af8e-bb886170701d">IBDA_DiseqCommand::put_DiseqSendCommand</a>.


### -param pulcbResponseLen [in, out]

On input, specifies the size of the <i>pbResponse</i> array, in bytes. On output, receives the number of bytes of data written into the <i>pbResponse</i> buffer.


### -param pbResponse [in, out]

Pointer to a byte array that receives the driver's response.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>BDA_E_BUFFER_TOO_SMALL</b></b></dt>
</dl>
</td>
<td width="60%">
The buffer given in the <i>pbResponse</i> parameter is too small.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0148a32d-b131-46ba-bbf0-82e2cf9c7d86">IBDA_DiseqCommand</a>
 

 

