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

# _DHCP_BIND_ELEMENT structure


## -description


The <b>DHCP_BIND_ELEMENT</b> structure defines an individual network binding for the DHCP server. A single DHCP server can contain multiple bindings and serve multiple networks.


## -struct-fields




### -field Flags

Specifies a set of bit flags indicating properties of the network binding.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_ENDPOINT_FLAG_CANT_MODIFY"></a><a id="dhcp_endpoint_flag_cant_modify"></a><dl>
<dt><b>DHCP_ENDPOINT_FLAG_CANT_MODIFY</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The binding specified in this structure cannot be modified.

</td>
</tr>
</table>
 


### -field fBoundToDHCPServer

Specifies whether or not this binding is set on the DHCP server. If <b>TRUE</b>, the binding is set; if <b>FALSE</b>, it is not.


### -field AdapterPrimaryAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the IP address assigned to the ethernet adapter of the DHCP server.


### -field AdapterSubnetAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the subnet IP mask used by this ethernet adapter.


### -field IfDescription

Unicode string that specifies the name assigned to this network interface device.


### -field IfIdSize

Specifies the size of the network interface device ID, in bytes.


### -field IfId

Specifies the network interface device ID.


### -field IfId.size_is

 


### -field IfId.size_is.IfIdSize

 




## -see-also




<a href="https://msdn.microsoft.com/9e43b2ab-f69d-4024-b6b1-8a36a3577767">DHCP_BIND_ELEMENT_ARRAY</a>
 

 

