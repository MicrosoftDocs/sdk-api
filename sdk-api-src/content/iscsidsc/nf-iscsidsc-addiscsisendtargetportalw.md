---
UID: NF:iscsidsc.AddIScsiSendTargetPortalW
title: AddIScsiSendTargetPortalW function (iscsidsc.h)
description: AddIscsiSendTargetPortal function adds a static target portal to the list of target portals to which the iSCSI initiator service transmits SendTargets requests. (Unicode)
helpviewer_keywords: ["AddIScsiSendTargetPortalW", "AddIscsiSendTargetPortal", "AddIscsiSendTargetPortal function [iSCSI Discovery Library API]", "AddIscsiSendTargetPortalW", "ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED", "ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED", "ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED", "ISCSI_SECURITY_FLAG_PFS_ENABLED", "ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED", "ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED", "ISCSI_SECURITY_FLAG_VALID", "iscsidisc.addiscsisendtargetportal", "iscsidsc/AddIscsiSendTargetPortal", "iscsidsc/AddIscsiSendTargetPortalW"]
old-location: iscsidisc\addiscsisendtargetportal.htm
tech.root: iSCSIDisc
ms.assetid: 8ca378bd-400d-40f1-81d2-c8b4135a3d3c
ms.date: 12/05/2018
ms.keywords: AddIScsiSendTargetPortalW, AddIscsiSendTargetPortal, AddIscsiSendTargetPortal function [iSCSI Discovery Library API], AddIscsiSendTargetPortalA, AddIscsiSendTargetPortalW, ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, iscsidisc.addiscsisendtargetportal, iscsidsc/AddIscsiSendTargetPortal, iscsidsc/AddIscsiSendTargetPortalA, iscsidsc/AddIscsiSendTargetPortalW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddIscsiSendTargetPortalW (Unicode) and AddIscsiSendTargetPortalA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddIScsiSendTargetPortalW
 - iscsidsc/AddIScsiSendTargetPortalW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - AddIscsiSendTargetPortal
 - AddIscsiSendTargetPortalA
 - AddIscsiSendTargetPortalW
---

# AddIScsiSendTargetPortalW function


## -description

The <b>AddIscsiSendTargetPortal</b> function adds a static target portal to the list of target portals to which the iSCSI initiator service transmits <b>SendTargets</b> requests.

## -parameters

### -param InitiatorInstance [in, optional]

The initiator that the iSCSI initiator service utilizes to transmit <b>SendTargets</b> requests to the specified target portal. If <b>null</b>, the iSCSI initiator service will use any initiator that can reach the target portal.

### -param InitiatorPortNumber [in, optional]

The port number to use for the <b>SendTargets</b> request. This port number corresponds to the source IP address on the Host-Bus Adapter (HBA).  A value of <b>ISCSI_ALL_INITIATOR_PORTS</b> indicates that the initiator must select the appropriate port based upon current routing information.

### -param LoginOptions [in, optional]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a> that contains the login options to use with the target portal.

### -param SecurityFlags [in, optional]

A bitmap that specifies the characteristics of the IPsec connection that the initiator adds to the session. If IPsec security policy between the initiator and the target portal is already configured as a result  of the portal group policy or a previous connection to the portal, the existing configuration takes precedence over the configuration specified in SecurityFlags and the security bitmap is ignored. 

If the <b>ISCSI_SECURITY_FLAG_VALID</b> flag is set to 0, the iSCSI initiator service uses default values for the security flags that are defined in the registry.

Caller can set any of the following flags in the bitmap:

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
When set to 1, the initiator should make the connection in IPsec tunnel mode. Caller should set this flag or the ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED flag, but not both.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED"></a><a id="iscsi_security_flag_transport_mode_preferred"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection in IPsec transport mode. Caller should set this flag or the ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED flag, but not both.

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
When set to 1, the initiator should make the connection with aggressive mode enabled. Caller should set this flag or the ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED flag, but not both. 



<div class="alert"><b>Note</b>  The Microsoft software initiator driver does not support aggressive mode.
</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED"></a><a id="iscsi_security_flag_main_mode_enabled"></a><dl>
<dt><b>ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
When set to 1, the initiator should make the connection with main mode enabled. Caller should set this flag or the ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED flag, but not both.

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

### -param Portal

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a> that indicates the portal to which SendTargets will be sent for target discovery.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines AddIScsiSendTargetPortal as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
