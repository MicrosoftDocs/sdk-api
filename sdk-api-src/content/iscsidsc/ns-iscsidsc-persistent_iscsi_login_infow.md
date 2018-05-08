---
UID: NS:iscsidsc.PERSISTENT_ISCSI_LOGIN_INFOW
title: PERSISTENT_ISCSI_LOGIN_INFOW
author: windows-driver-content
description: PERSISTENT_ISCSI_LOGIN_INFO structure contains information that describes a login session established by the Microsoft iSCSI initiator service after the machine boots up.
old-location: iscsidisc\persistent_iscsi_login_info.htm
old-project: iSCSIDisc
ms.assetid: adfd57fb-18dc-440f-988e-f2c01698d987
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PPERSISTENT_ISCSI_LOGIN_INFOW, ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, PERSISTENT_ISCSI_LOGIN_INFO, PERSISTENT_ISCSI_LOGIN_INFO structure [iSCSI Discovery Library API], PERSISTENT_ISCSI_LOGIN_INFOA, PERSISTENT_ISCSI_LOGIN_INFOW, PPERSISTENT_ISCSI_LOGIN_INFO, PPERSISTENT_ISCSI_LOGIN_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.persistent_iscsi_login_info, iscsidsc/PERSISTENT_ISCSI_LOGIN_INFO, iscsidsc/PERSISTENT_ISCSI_LOGIN_INFOA, iscsidsc/PERSISTENT_ISCSI_LOGIN_INFOW, iscsidsc/PPERSISTENT_ISCSI_LOGIN_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PERSISTENT_ISCSI_LOGIN_INFOW (Unicode) and PERSISTENT_ISCSI_LOGIN_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PERSISTENT_ISCSI_LOGIN_INFOW, *PPERSISTENT_ISCSI_LOGIN_INFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iscsidsc.h
api_name:
-	PERSISTENT_ISCSI_LOGIN_INFO
-	PERSISTENT_ISCSI_LOGIN_INFOA
-	PERSISTENT_ISCSI_LOGIN_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# PERSISTENT_ISCSI_LOGIN_INFOW structure


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
 

 

