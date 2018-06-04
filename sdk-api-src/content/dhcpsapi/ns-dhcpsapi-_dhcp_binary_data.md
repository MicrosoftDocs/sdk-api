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

# _DHCP_BINARY_DATA structure


## -description


The <b>DHCP_BINARY_DATA</b> structure defines an opaque blob of binary data.


## -struct-fields




### -field DataLength

Specifies the size of <b>Data</b>, in bytes.


### -field Data

Pointer to an opaque blob of byte (binary) data.

The data is formatted as follows:

<table>
<tr>
<th>Byte</th>
<th>Format</th>
</tr>
<tr>
<td>Byte 0 to byte 3 </td>
<td>The result of a binary AND on the IP address and the subnet mask in reverse order.</td>
</tr>
<tr>
<td>Byte 4</td>
<td>Hardware identifier. This value is always 0x01.</td>
</tr>
<tr>
<td>Byte 5 to Byte 10 </td>
<td>The MAC address of the client.</td>
</tr>
</table>
 


### -field Data.size_is

 


### -field Data.size_is.DataLength

 



