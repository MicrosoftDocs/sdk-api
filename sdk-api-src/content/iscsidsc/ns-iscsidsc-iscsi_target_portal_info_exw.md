---
UID: NS:iscsidsc.__unnamed_struct_10
title: ISCSI_TARGET_PORTAL_INFO_EXW (iscsidsc.h)
author: windows-sdk-content
description: The ISCSI_TARGET_PORTAL_INFO_EX structure contains information about login credentials to a target portal.
old-location: iscsidisc\iscsi_target_portal_info_ex.htm
tech.root: iSCSIDisc
ms.assetid: 1c7035db-a71d-43b5-8595-82097ae5433d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PISCSI_TARGET_PORTAL_INFO_EXW, ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, ISCSI_TARGET_PORTAL_INFO_EX, ISCSI_TARGET_PORTAL_INFO_EX structure [iSCSI Discovery Library API], ISCSI_TARGET_PORTAL_INFO_EXA, ISCSI_TARGET_PORTAL_INFO_EXW, PISCSI_TARGET_PORTAL_INFO_EX, PISCSI_TARGET_PORTAL_INFO_EX structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_target_portal_info_ex, iscsidsc/ISCSI_TARGET_PORTAL_INFO_EX, iscsidsc/ISCSI_TARGET_PORTAL_INFO_EXA, iscsidsc/ISCSI_TARGET_PORTAL_INFO_EXW, iscsidsc/PISCSI_TARGET_PORTAL_INFO_EX"
ms.topic: struct
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_TARGET_PORTAL_INFO_EXW (Unicode) and ISCSI_TARGET_PORTAL_INFO_EXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - ISCSI_TARGET_PORTAL_INFO_EX
 - ISCSI_TARGET_PORTAL_INFO_EXA
 - ISCSI_TARGET_PORTAL_INFO_EXW
product: Windows
targetos: Windows
req.typenames: ISCSI_TARGET_PORTAL_INFO_EXW, *PISCSI_TARGET_PORTAL_INFO_EXW
req.redist: 
---

# ISCSI_TARGET_PORTAL_INFO_EXW structure


## -description


The <b>ISCSI_TARGET_PORTAL_INFO_EX</b> structure contains information about login credentials to a target portal.


## -struct-fields




### -field InitiatorName

A string that represents the name of the Host-Bus Adapter (HBA) initiator.


### -field InitiatorPortNumber

A <b>ULONG</b>  value that represents the port number on the HBA associated with the portal.


### -field SymbolicName

A string that represents the symbolic name associated with the portal.


### -field Address

A string that represents the IP address or DNS name associated with the portal.


### -field Socket

A <b>USHORT</b> value that represents the socket number.


### -field SecurityFlags

A pointer to an <b>ISCSI_SECURITY_FLAGS</b> structure that contains a bitmap that defines the security charactaristics of a login connection.

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
When set to 1, the initiator should make the connection in IPsec tunnel mode. Caller should set this flag or the <b>ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED</b> flag, but not both.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED"></a><a id="iscsi_security_flag_transport_mode_preferred"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection in IPsec transport mode. Caller should set this flag or the <b>ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED</b> flag, but not both.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_PFS_ENABLED"></a><a id="iscsi_security_flag_pfs_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_PFS_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with Perfect Forward Secrecy (PFS) mode enabled; otherwise, the initiator should make the connection with PFS mode disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED"></a><a id="iscsi_security_flag_aggressive_mode_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with aggressive mode enabled. Caller should set this flag or the <b>ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED</b> flag, but not both. 



<div class="alert"><b>Note</b>  The Microsoft software initiator driver does not support aggressive mode.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED"></a><a id="iscsi_security_flag_main_mode_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with main mode enabled. Caller should set this flag or the <b>ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED</b> flag, but not both.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED"></a><a id="iscsi_security_flag_ike_ipsec_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with the IKE/IPsec protocol enabled; otherwise, the IKE/IPsec protocol is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_VALID"></a><a id="iscsi_security_flag_valid"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_VALID</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the other mask values are valid; otherwise, the iSCSI initiator service will use bitmap values that were previously defined for the target portal, or if none are available, the initiator service uses the default values defined in the registry. 

</td>
</tr>
</table>
 


### -field LoginOptions

A pointer to an <a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a> structure that defines the login data.


## -see-also




<a href="https://msdn.microsoft.com/3592b289-9c0d-43dc-918f-23c8ff079186">ISCSI_TARGET_PORTAL_INFO</a>
 

 

