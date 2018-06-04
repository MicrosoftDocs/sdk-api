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

# IKE_AUTHENTICATION_PRESHARED_KEY structure


## -description


The <b>IKE_AUTHENTICATION_PRESHARED_KEY</b> structure contains information about the preshared key used in the Internet Key Exchange (IKE) protocol. 



## -struct-fields




### -field SecurityFlags

A bitmap that defines the security characteristics of a login connection. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED"></a><a id="iscsi_security_flag_tunnel_mode_preferred"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED</b></dt>
</dl>
</td>
<td width="60%">
The Host Bus Adapter (HBA) initiator should establish the TCP/IP connection to the target portal using IPsec tunnel mode. 

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED"></a><a id="iscsi_security_flag_transport_mode_preferred"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED</b></dt>
</dl>
</td>
<td width="60%">
The HBA initiator should establish the TCP/IP connection to the target portal using IPsec transport mode.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_PFS_ENABLED"></a><a id="iscsi_security_flag_pfs_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_PFS_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The HBA initiator should establish the TCP/IP connection to the target portal with Perfect Forward Secrecy (PFS) mode enabled if IPsec is required.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED"></a><a id="iscsi_security_flag_aggressive_mode_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The HBA initiator should establish the TCP/IP connection to the target portal with aggressive mode enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED"></a><a id="iscsi_security_flag_main_mode_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The HBA initiator should establish the TCP/IP connection to the target portal with main mode enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED"></a><a id="iscsi_security_flag_ike_ipsec_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The HBA initiator should establish the TCP/IP connection to the target portal using IKE/IPsec protocol. If not set then IPsec is not required to login to the target.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_VALID"></a><a id="iscsi_security_flag_valid"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_VALID</b></dt>
</dl>
</td>
<td width="60%">
The other mask values are valid; otherwise, security flags are not specified.

</td>
</tr>
</table>
 


### -field IdType

The type of key identifier. The following table specifies the values that can be assigned to this member:

<table>
<tr>
<th>ID Types</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ID_IPV4_ADDR"></a><a id="id_ipv4_addr"></a><dl>
<dt><b>ID_IPV4_ADDR</b></dt>
</dl>
</td>
<td width="60%">
Indicates four bytes of binary data that constitute a version 4 IP address. 

</td>
</tr>
<tr>
<td width="40%"><a id="ID_FQDN"></a><a id="id_fqdn"></a><dl>
<dt><b>ID_FQDN</b></dt>
</dl>
</td>
<td width="60%">
An ANSI string that contains a fully qualified domain name. This string does not contain terminators.

</td>
</tr>
<tr>
<td width="40%"><a id="ID_USER_FQDN"></a><a id="id_user_fqdn"></a><dl>
<dt><b>ID_USER_FQDN</b></dt>
</dl>
</td>
<td width="60%">
An ANSI string that contains a fully qualified user name. This string does not contain terminators.

</td>
</tr>
<tr>
<td width="40%"><a id="ID_IPV6_ADDR"></a><a id="id_ipv6_addr"></a><dl>
<dt><b>ID_IPV6_ADDR</b></dt>
</dl>
</td>
<td width="60%">
Indicates 16 bytes of binary data that constitute a version 6 IP address. 

</td>
</tr>
</table>
 


### -field IdLengthInBytes

The length, in bytes, of the key identifier.


### -field Id

The identifier of the preshared key used in the IKE protocol.


### -field KeyLengthInBytes

The length, in bytes, of the preshared key.


### -field Key

The preshared key.

