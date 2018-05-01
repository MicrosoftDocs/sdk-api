---
UID: NS:dhcpsapi._DHCP_ATTRIB
title: "_DHCP_ATTRIB"
author: windows-driver-content
description: Defines an attribute set on the DHCP server.
old-location: dhcp\dhcp_attrib.htm
old-project: DHCP
ms.assetid: 26822137-8633-4e18-a69f-eeebf9e78f9a
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCP_ATTRIB, *PDHCP_ATTRIB, DHCP_ATTRIB, DHCP_ATTRIB structure [DHCP], DHCP_ATTRIB_BOOL_IS_ADMIN, DHCP_ATTRIB_BOOL_IS_BINDING_AWARE, DHCP_ATTRIB_BOOL_IS_DYNBOOTP, DHCP_ATTRIB_BOOL_IS_PART_OF_DSDC, DHCP_ATTRIB_BOOL_IS_ROGUE, DHCP_ATTRIB_ULONG_RESTORE_STATUS, PDHCP_ATTRIB *LPDHCP_ATTRIB, PDHCP_ATTRIB *LPDHCP_ATTRIB structure pointer [DHCP], _DHCP_ATTRIB, dhcp.dhcp_attrib, dhcpsapi/PDHCP_ATTRIB *LPDHCP_ATTRIB, dhcpsapi/_DHCP_ATTRIB"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCP_ATTRIB, *PDHCP_ATTRIB, *LPDHCP_ATTRIB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_ATTRIB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 


## -remarks



A DHCP server attribute is a value that can be queried to determine supported and available features.



