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

# IBDA_MUX::GetPidList


## -description


Gets the list of packet identifiers (PIDs) that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.


## -parameters




### -param pulPidListCount [in, out]

On input, specifies the size, in array elements, of the <i>pbPidListBuffer</i> array. On output, receives the number of PIDs.


### -param pbPidListBuffer [in, out]

Pointer to an array of <a href="https://msdn.microsoft.com/50355317-7133-445c-9990-ab536801e555">BDA_MUX_PIDLISTITEM</a> structures. The method fills in the array with the list of PIDs.


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
<dt><b><b>E_NOT_SUFFICIENT_BUFFER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>pbPidListBuffer</i> array is too small.

</td>
</tr>
</table>
 




## -remarks



If the <i>pbPidListBuffer</i> array is too small, the method returns <b>E_NOT_SUFFICIENT_BUFFER</b> and sets the required size in the <i>pulPidListCount</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/5dde7b14-d5a4-4db5-b91f-d6bfd4be269d">IBDA_MUX</a>
 

 

