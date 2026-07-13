---
UID: NS:iscsidsc.PERSISTENT_ISCSI_LOGIN_INFOW
title: PERSISTENT_ISCSI_LOGIN_INFOW (iscsidsc.h)
description: PERSISTENT_ISCSI_LOGIN_INFO structure contains information that describes a login session established by the Microsoft iSCSI initiator service after the machine boots up. (Unicode)
helpviewer_keywords: ["*PPERSISTENT_ISCSI_LOGIN_INFOW","ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED","ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED","ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED","ISCSI_SECURITY_FLAG_PFS_ENABLED","ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED","ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED","ISCSI_SECURITY_FLAG_VALID","PERSISTENT_ISCSI_LOGIN_INFO","PERSISTENT_ISCSI_LOGIN_INFO structure [iSCSI Discovery Library API]","PERSISTENT_ISCSI_LOGIN_INFOA","PERSISTENT_ISCSI_LOGIN_INFOW","PPERSISTENT_ISCSI_LOGIN_INFO","PPERSISTENT_ISCSI_LOGIN_INFO structure pointer [iSCSI Discovery Library API]","iscsidisc.persistent_iscsi_login_info","iscsidsc/PERSISTENT_ISCSI_LOGIN_INFO","iscsidsc/PERSISTENT_ISCSI_LOGIN_INFOA","iscsidsc/PERSISTENT_ISCSI_LOGIN_INFOW","iscsidsc/PPERSISTENT_ISCSI_LOGIN_INFO"]
old-location: iscsidisc\persistent_iscsi_login_info.htm
tech.root: iSCSIDisc
ms.assetid: adfd57fb-18dc-440f-988e-f2c01698d987
ms.date: 12/05/2018
ms.keywords: '*PPERSISTENT_ISCSI_LOGIN_INFOW, ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, PERSISTENT_ISCSI_LOGIN_INFO, PERSISTENT_ISCSI_LOGIN_INFO structure [iSCSI Discovery Library API], PERSISTENT_ISCSI_LOGIN_INFOA, PERSISTENT_ISCSI_LOGIN_INFOW, PPERSISTENT_ISCSI_LOGIN_INFO, PPERSISTENT_ISCSI_LOGIN_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.persistent_iscsi_login_info, iscsidsc/PERSISTENT_ISCSI_LOGIN_INFO, iscsidsc/PERSISTENT_ISCSI_LOGIN_INFOA, iscsidsc/PERSISTENT_ISCSI_LOGIN_INFOW, iscsidsc/PPERSISTENT_ISCSI_LOGIN_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PERSISTENT_ISCSI_LOGIN_INFOW, *PPERSISTENT_ISCSI_LOGIN_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PPERSISTENT_ISCSI_LOGIN_INFOW
 - iscsidsc/PPERSISTENT_ISCSI_LOGIN_INFOW
 - PERSISTENT_ISCSI_LOGIN_INFOW
 - iscsidsc/PERSISTENT_ISCSI_LOGIN_INFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - PERSISTENT_ISCSI_LOGIN_INFO
 - PERSISTENT_ISCSI_LOGIN_INFOA
 - PERSISTENT_ISCSI_LOGIN_INFOW
---

# PERSISTENT_ISCSI_LOGIN_INFOW structure


## -description

The <b>PERSISTENT_ISCSI_LOGIN_INFO</b> structure contains information that describes a login session established by the Microsoft iSCSI initiator service after the machine boots up.

## -struct-fields

### -field TargetName

A string representing the name of the target the initiator will login to.

### -field IsInformationalSession

If set <b>TRUE</b>, the login session is for informational purposes only and will not result in the enumeration of the specified target on the local computer. For an informational login session, the LUNs on the target are not reported to the Plug and Play Manager and the device drivers for the target are not loaded.

A management application can still access targets not enumerated by the system via the <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsiinquiry">SendScsiInquiry</a>, <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsireportluns">SendScsiReportLuns</a>, and <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsireadcapacity">SendScsiReadCapcity</a> functions.

If set <b>FALSE</b>, the LUNs on the target are reported to the Plug and Play manager for enumeration.

### -field InitiatorInstance

A string representing the name of the initiator used to login to the target.

### -field InitiatorPortNumber

The port number of the Host-Bus Adapter (HBA) through which the session login is established. A value of <b>ISCSI_ANY_INITIATOR_PORT</b> indicates that a port on the initiator is not currently specified.

### -field TargetPortal

A <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a> structure that describes the portal used by the Microsoft iSCSI initiator service to log on to the target.

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

A pointer to a <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a> structure that contains information about a target, its logical units, HBAs, and buses through which it is reached.

### -field LoginOptions

An <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a> structure that contains the persistent login characteristics.

## -remarks

The <b>PERSISTENT_ISCSI_LOGIN_INFO</b> structure is used in conjunction with the <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIScsiPersistentLogins</a> function to retrieve the list of targets for which the Microsoft Discovery Service (iscsiexe.exe) automatically opens a login session after the machine boots up.





> [!NOTE]
> The iscsidsc.h header defines PERSISTENT_ISCSI_LOGIN_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIScsiPersistentLogins</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsiinquiry">SendScsiInquiry</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsireadcapacity">SendScsiReadCapacity</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsireportluns">SendScsiReportLuns</a>

