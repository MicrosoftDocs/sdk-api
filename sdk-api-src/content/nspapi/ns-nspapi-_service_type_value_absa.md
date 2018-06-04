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

# _SERVICE_TYPE_VALUE_ABSA structure


## -description



			The 
<b>SERVICE_TYPE_VALUE_ABS</b> structure contains information about a network-service type value. This information may be specific to a namespace.


## -struct-fields




### -field dwNameSpace

Type: <b>DWORD</b>

A namespace, or a set of default namespaces, for which the network service type value is intended. Namespace providers will look only at values intended for their namespace. 




Use one of the following constants to specify a namespace:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_DEFAULT"></a><a id="ns_default"></a><dl>
<dt><b>NS_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
A set of default namespaces. The function queries each namespace within this set. The set of default namespaces typically includes all the namespaces installed on the system. System administrators, however, can exclude particular namespaces from the set. NS_DEFAULT is the value that most applications should use for <b>dwNameSpace</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The Domain Name System used in the Internet for host name resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NETBT"></a><a id="ns_netbt"></a><dl>
<dt><b>NS_NETBT</b></dt>
</dl>
</td>
<td width="60%">
The NetBIOS over TCP/IP layer. All Windows operating systems register their computer names with NetBIOS. This namespace is used to convert a computer name to an IP address that uses this registration. Note that NS_NETBT may access a WINS server to perform the resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_SAP"></a><a id="ns_sap"></a><dl>
<dt><b>NS_SAP</b></dt>
</dl>
</td>
<td width="60%">
The NetWare Service Advertising Protocol. This may access the NetWare bindery if appropriate. NS_SAP is a dynamic namespace that allows registration of services.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_HOSTS"></a><a id="ns_tcpip_hosts"></a><dl>
<dt><b>NS_TCPIP_HOSTS</b></dt>
</dl>
</td>
<td width="60%">
Lookup value in the &lt;systemroot&gt;\system32\drivers\etc\hosts file.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_LOCAL"></a><a id="ns_tcpip_local"></a><dl>
<dt><b>NS_TCPIP_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Local TCP/IP name resolution mechanisms, including comparisons against the local host name and looks up host names and IP addresses in cache of host to IP address mappings.

</td>
</tr>
</table>
 


### -field dwValueType

Type: <b>DWORD</b>

The type of the value data. Specify one of the following types: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_BINARY"></a><a id="reg_binary"></a><dl>
<dt><b>REG_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary data in any form.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_DWORD"></a><a id="reg_dword"></a><dl>
<dt><b>REG_DWORD</b></dt>
</dl>
</td>
<td width="60%">
A 32-bit number.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_MULTI_SZ"></a><a id="reg_multi_sz"></a><dl>
<dt><b>REG_MULTI_SZ</b></dt>
</dl>
</td>
<td width="60%">
An array of null-terminated strings, terminated by two null characters.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_SZ"></a><a id="reg_sz"></a><dl>
<dt><b>REG_SZ</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string.

</td>
</tr>
</table>
 


### -field dwValueSize

Type: <b>DWORD</b>

The size, in bytes,  of the value pointed to by the <b>lpValue</b> member. In the case of REG_SZ and REG_MULTI_SZ string data, the terminating characters are counted as part of the size.


### -field lpValueName

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated string that is the name of the value. This name is specific to a namespace. 




Several commonly used value name strings are associated with defined constants. These name strings include the following.

<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TYPE_VALUE_SAPID"></a><a id="service_type_value_sapid"></a><dl>
<dt><b>SERVICE_TYPE_VALUE_SAPID</b></dt>
</dl>
</td>
<td width="60%">
"SapId"

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TYPE_VALUE_CONN"></a><a id="service_type_value_conn"></a><dl>
<dt><b>SERVICE_TYPE_VALUE_CONN</b></dt>
</dl>
</td>
<td width="60%">
"ConnectionOriented"

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TYPE_VALUE_TCPPORT"></a><a id="service_type_value_tcpport"></a><dl>
<dt><b>SERVICE_TYPE_VALUE_TCPPORT</b></dt>
</dl>
</td>
<td width="60%">
"TcpPort"

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TYPE_VALUE_UDPPORT"></a><a id="service_type_value_udpport"></a><dl>
<dt><b>SERVICE_TYPE_VALUE_UDPPORT</b></dt>
</dl>
</td>
<td width="60%">
"UdpPort"

</td>
</tr>
</table>
 


### -field lpValue

Type: <b>PVOID</b>

A pointer to the value data.


## -remarks



When you use the 
<a href="https://msdn.microsoft.com/cc5e35ef-5c64-41ba-a5f9-5961371c4d08">SetService</a> function to add a network service type to a namespace, a 
<a href="https://msdn.microsoft.com/9adf92b0-1268-48c1-91e4-d05ad696ff06">SERVICE_TYPE_INFO_ABS</a> structure is passed as the <b>ServiceSpecificInfo</b> BLOB member of a 
<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a> structure. Although the <b>ServiceSpecificInfo</b> member generally should not contain pointers, an exception is made in the case of the 
<b>SERVICE_TYPE_INFO_ABS</b> and 
<b>SERVICE_TYPE_VALUE_ABS</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/9adf92b0-1268-48c1-91e4-d05ad696ff06">SERVICE_TYPE_INFO_ABS</a>



<a href="https://msdn.microsoft.com/cc5e35ef-5c64-41ba-a5f9-5961371c4d08">SetService</a>
 

 

