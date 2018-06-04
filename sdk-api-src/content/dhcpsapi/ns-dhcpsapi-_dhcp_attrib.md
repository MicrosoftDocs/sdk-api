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

# _DHCP_ATTRIB structure


## -description


The <b>DHCP_ATTRIB</b> structure defines an attribute set on the DHCP server.


## -struct-fields




### -field DhcpAttribId


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_ATTRIB_ID</a> structure that uniquely identifies the DHCP server attribute.


### -field DhcpAttribType

Specifies exactly one of the following attribute types.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_ATTRIB_BOOL_IS_ROGUE"></a><a id="dhcp_attrib_bool_is_rogue"></a><dl>
<dt><b>DHCP_ATTRIB_BOOL_IS_ROGUE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The DHCP server is rogue.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_ATTRIB_BOOL_IS_DYNBOOTP"></a><a id="dhcp_attrib_bool_is_dynbootp"></a><dl>
<dt><b>DHCP_ATTRIB_BOOL_IS_DYNBOOTP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The DHCP server supports BOOTP for dynamic address service.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_ATTRIB_BOOL_IS_PART_OF_DSDC"></a><a id="dhcp_attrib_bool_is_part_of_dsdc"></a><dl>
<dt><b>DHCP_ATTRIB_BOOL_IS_PART_OF_DSDC</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
The DHCP server is part of the directory service domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_ATTRIB_BOOL_IS_BINDING_AWARE"></a><a id="dhcp_attrib_bool_is_binding_aware"></a><dl>
<dt><b>DHCP_ATTRIB_BOOL_IS_BINDING_AWARE</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
The DHCP server is binding aware.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_ATTRIB_BOOL_IS_ADMIN"></a><a id="dhcp_attrib_bool_is_admin"></a><dl>
<dt><b>DHCP_ATTRIB_BOOL_IS_ADMIN</b></dt>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
The DHCP server is the admin-level DHCP server.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_ATTRIB_ULONG_RESTORE_STATUS"></a><a id="dhcp_attrib_ulong_restore_status"></a><dl>
<dt><b>DHCP_ATTRIB_ULONG_RESTORE_STATUS</b></dt>
<dt>0x06</dt>
</dl>
</td>
<td width="60%">
The DHCP server can restore status with the provided attribute value.

</td>
</tr>
</table>
 


### -field DhcpAttribBool.case

 


### -field DhcpAttribBool.case.DHCP_ATTRIB_TYPE_BOOL

 


### -field DhcpAttribUlong.case

 


### -field DhcpAttribUlong.case.DHCP_ATTRIB_TYPE_ULONG

 


### -field switch_is

 


### -field switch_is.DhcpAttribType

 


### -field switch_type

 


### -field switch_type.ULONG

 


### -field DhcpAttribBool

 


### -field DhcpAttribUlong

 




## -remarks



A DHCP server attribute is a value that can be queried to determine supported and available features.



