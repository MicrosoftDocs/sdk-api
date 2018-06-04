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

# ITMSPAddress::ReceiveTSPData


## -description


The 
<b>ReceiveTSPData</b> method is called by TAPI 3 when the TSP sends asynchronous data to the MSP. If the TSP sends the 
<a href="https://msdn.microsoft.com/982f40b3-7758-493c-9d04-6480e3c9e86d">LINE_SENDMSPDATA</a> message with the <b>htCall</b> set to <b>NULL</b>, <i>pMSPCall</i> will be <b>NULL</b>. If the TSP does specify the <b>htCall</b>, <i>pMSPCall</i> will correspond to the call created in 
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>.


## -parameters




### -param pMSPCall [in]

Pointer to <a href="_com_iunknown">IUnknown</a> interface of the MSP Call object.


### -param pBuffer

[in, size_is(<i>dwSize</i>)] Pointer to opaque buffer from the TSP.


### -param dwSize [in]

Size, in bytes, of <i>pBuffer</i>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pMSPCall</i> or <i>pBuffer</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pMSPCall</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pMSPCall</i> parameter does not point to a valid interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The MSP must free memory in <i>pBuffer</i>.

The semantics of the data passed in the buffer are specific to each TSP/MSP pair. This method simply dispatches the received buffer to the address (<i>pMSPCall</i> == <b>NULL</b>) or the indicated call (<i>pMSPCall</i> != <b>NULL</b>).




## -see-also




<a href="https://msdn.microsoft.com/246a0bcd-0dbb-4b77-a1cd-e6378eaff889">ITMSPAddress</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

