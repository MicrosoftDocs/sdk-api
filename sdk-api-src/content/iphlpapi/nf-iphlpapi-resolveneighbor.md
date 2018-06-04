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

# ResolveNeighbor function


## -description


<p class="CCE_Message">[<b>ResolveNeighbor</b> is no longer available for use as of Windows Vista. Instead, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff570686">ResolveIpNetEntry2</a>.]

The 
<b>ResolveNeighbor</b> function  resolves the physical address for a neighbor IP address entry on the local computer.


## -parameters




### -param NetworkAddress [in]

A pointer to a   <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a> structure that contains the neighbor IP address entry and address family.


### -param PhysicalAddress [out]

A pointer to a byte array buffer that will receive the physical address that corresponds to the IP address specified by the <i>NetworkAddress</i> parameter if the function is successful. The length of the byte array is passed in the <i>PhysicalAddressLength</i> parameter.


### -param PhysicalAddressLength [in, out]

On input, this parameter specifies the maximum length, in bytes, of the buffer passed in the <i>PhysicalAddress</i> parameter to receive the physical address. If the function is successful, this parameter will receive the length of the physical address returned in the buffer pointed to by the <i>PhysicalAddress</i> parameter. If <b>ERROR_BUFFER_OVERFLOW</b> is returned, this parameter contains the number of bytes
        required to hold the physical address.


## -returns



The <b>ResolveNeighbor</b> function always fails and returns the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570686">ResolveIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>
 

 

