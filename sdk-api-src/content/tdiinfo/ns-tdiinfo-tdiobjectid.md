---
UID: NS:tdiinfo.TDIObjectID
title: TDIObjectID
author: windows-driver-content
description: Contains a part of the TCP_REQUEST_QUERY_INFORMATION_EX structure that is used with the IOCTL_TCP_QUERY_INFORMATION_EX control code to specify the kind of information being requested from the TCP driver.
old-location: winprog\tdiobjectid.htm
old-project: DevNotes
ms.assetid: 79d34f1c-2ea7-4867-9fb2-80401b0859bf
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ENTITY_LIST_ID, ENTITY_TYPE_ID, IF_MIB_STATS_ID, INFO_CLASS_GENERIC, INFO_CLASS_PROTOCOL, INFO_TYPE_ADDRESS_OBJECT, INFO_TYPE_CONNECTION, INFO_TYPE_PROVIDER, IP_INTFC_INFO_ID, IP_MIB_ADDRTABLE_ENTRY_ID, IP_MIB_STATS_ID, TDIObjectID, TDIObjectID structure [Windows API], tdiinfo/TDIObjectID, winprog.tdiobjectid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tdiinfo.h
req.include-header: 
req.target-type: Windows
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
req.typenames: TDIObjectID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	tdiinfo.h
api_name:
-	TDIObjectID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TDIObjectID structure


## -description


<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Contains a part of the  <a href="https://msdn.microsoft.com/2a1f3a41-ee18-4a67-9da1-a5b18d32defb">TCP_REQUEST_QUERY_INFORMATION_EX</a> structure that is used with the <a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a> control code to specify the kind of  information being requested from the TCP driver.


## -struct-fields




### -field toi_entity

This is a <a href="https://msdn.microsoft.com/d95a96b5-c062-44c5-9a66-b27db531800a">TDIEntityID</a> structure.


### -field toi_class

The kind of information being requested. The value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INFO_CLASS_GENERIC"></a><a id="info_class_generic"></a><dl>
<dt><b>INFO_CLASS_GENERIC</b></dt>
</dl>
</td>
<td width="60%">
Used when requesting an enumeration of all TDI entities on the current machine, or when determining the type of one of those TDI entities.

</td>
</tr>
<tr>
<td width="40%"><a id="INFO_CLASS_PROTOCOL"></a><a id="info_class_protocol"></a><dl>
<dt><b>INFO_CLASS_PROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
Used when requesting information about a specific interface or IP entity.

</td>
</tr>
</table>
 


### -field toi_type

The type of object being queried. The value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INFO_TYPE_PROVIDER"></a><a id="info_type_provider"></a><dl>
<dt><b>INFO_TYPE_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
A service provider. All queries described in the <a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a> topic use this type value.

</td>
</tr>
<tr>
<td width="40%"><a id="INFO_TYPE_ADDRESS_OBJECT"></a><a id="info_type_address_object"></a><dl>
<dt><b>INFO_TYPE_ADDRESS_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
An address object.

</td>
</tr>
<tr>
<td width="40%"><a id="INFO_TYPE_CONNECTION"></a><a id="info_type_connection"></a><dl>
<dt><b>INFO_TYPE_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
A connection object.

</td>
</tr>
</table>
 


### -field toi_id

 If <b>toi_class</b> is <b>INFO_CLASS_GENERIC</b>, <b>toi_id</b> can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENTITY_LIST_ID"></a><a id="entity_list_id"></a><dl>
<dt><b>ENTITY_LIST_ID</b></dt>
</dl>
</td>
<td width="60%">
The query returns a list of all TDI entities on the local machine.

</td>
</tr>
<tr>
<td width="40%"><a id="ENTITY_TYPE_ID"></a><a id="entity_type_id"></a><dl>
<dt><b>ENTITY_TYPE_ID</b></dt>
</dl>
</td>
<td width="60%">
The query returns a type value for a specified TDI entity.

</td>
</tr>
</table>
 

If <b>toi_class</b> is <b>INFO_CLASS_PROTOCOL</b>, <b>toi_id</b> can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IF_MIB_STATS_ID"></a><a id="if_mib_stats_id"></a><dl>
<dt><b>IF_MIB_STATS_ID</b></dt>
</dl>
</td>
<td width="60%">
When the entity being queried is an interface supporting MIB-II, causes the query to return an <a href="https://msdn.microsoft.com/830cd19e-06a9-46dc-a869-d2a17107d942">IFEntry</a> structure that contains information about the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_MIB_STATS_ID"></a><a id="ip_mib_stats_id"></a><dl>
<dt><b>IP_MIB_STATS_ID</b></dt>
</dl>
</td>
<td width="60%">
When the entity being queried is a network-layer IP entity, causes the query to return an <a href="https://msdn.microsoft.com/eb25fae9-1a89-4474-bcb6-28c09bc3e0c9">IPSNMPInfo</a> structure that contains information about the entity.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_MIB_ADDRTABLE_ENTRY_ID"></a><a id="ip_mib_addrtable_entry_id"></a><dl>
<dt><b>IP_MIB_ADDRTABLE_ENTRY_ID</b></dt>
</dl>
</td>
<td width="60%">
When the entity being queried is a network-layer IP entity on which one or more IP addresses are active, causes the query to return an array of <a href="https://msdn.microsoft.com/c48453e8-05f1-49d8-bae6-fad0681bdf7e">IPAddrEntry</a> structures that contain information about those addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_INTFC_INFO_ID"></a><a id="ip_intfc_info_id"></a><dl>
<dt><b>IP_INTFC_INFO_ID</b></dt>
</dl>
</td>
<td width="60%">
Causes an <a href="https://msdn.microsoft.com/dc9de369-f739-475c-96f5-e2e058705fe8">IPInterfaceInfo</a> structure to be returned with information about a specific IP address specified in the <b>Context</b> member of the <a href="https://msdn.microsoft.com/2a1f3a41-ee18-4a67-9da1-a5b18d32defb">TCP_REQUEST_QUERY_INFORMATION_EX</a> structure.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/566bf187-73d0-4d61-be8e-306dc482a005">Management Information Base
			 Reference</a>
 

 

