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

# PERSISTENT_ISCSI_LOGIN_INFOA structure


## -description


The <b>PERSISTENT_ISCSI_LOGIN_INFO</b> structure contains information that describes a login session established by the Microsoft iSCSI initiator service after the machine boots up.


## -struct-fields




### -field TargetName

A string representing the name of the target the initiator will login to.


### -field IsInformationalSession

If set <b>TRUE</b>, the login session is for informational purposes only and will not result in the enumeration of the specified target on the local computer. For an informational login session, the LUNs on the target are not reported to the Plug and Play Manager and the device drivers for the target are not loaded.

A management application can still access targets not enumerated by the system via the <a href="https://msdn.microsoft.com/a1339ff0-aa1e-4609-8983-d5f09481bd13">SendScsiInquiry</a>, <a href="https://msdn.microsoft.com/0898daf0-67ae-47a4-90bf-2112b6e6b20c">SendScsiReportLuns</a>, and <a href="https://msdn.microsoft.com/1a12848f-4b2d-45f6-971b-d8e4ccd00c21">SendScsiReadCapcity</a> functions.

If set <b>FALSE</b>, the LUNs on the target are reported to the Plug and Play manager for enumeration.


### -field InitiatorInstance

A string representing the name of the initiator used to login to the target.


### -field InitiatorPortNumber

The port number of the Host-Bus Adapter (HBA) through which the session login is established. A value of <b>ISCSI_ANY_INITIATOR_PORT</b> indicates that a port on the initiator is not currently specified.


### -field TargetPortal

A <a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a> structure that describes the portal used by the Microsoft iSCSI initiator service to log on to the target.


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
 


### -field Mappings

A pointer to a <a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a> structure that contains information about a target, its logical units, HBAs, and buses through which it is reached.


### -field LoginOptions

An <a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a> structure that contains the persistent login characteristics.


## -remarks



The <b>PERSISTENT_ISCSI_LOGIN_INFO</b> structure is used in conjunction with the <a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIScsiPersistentLogins</a> function to retrieve the list of targets for which the Microsoft Discovery Service (iscsiexe.exe) automatically opens a login session after the machine boots up.




## -see-also




<a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a>



<a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a>



<a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIScsiPersistentLogins</a>



<a href="https://msdn.microsoft.com/a1339ff0-aa1e-4609-8983-d5f09481bd13">SendScsiInquiry</a>



<a href="https://msdn.microsoft.com/1a12848f-4b2d-45f6-971b-d8e4ccd00c21">SendScsiReadCapacity</a>



<a href="https://msdn.microsoft.com/0898daf0-67ae-47a4-90bf-2112b6e6b20c">SendScsiReportLuns</a>
 

 

