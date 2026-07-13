---
UID: NF:iscsidsc.LoginIScsiTargetW
title: LoginIScsiTargetW function (iscsidsc.h)
description: LoginIscsiTarget function establishes a full featured login session with the indicated target. (Unicode)
helpviewer_keywords: ["ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED", "ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED", "ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED", "ISCSI_SECURITY_FLAG_PFS_ENABLED", "ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED", "ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED", "ISCSI_SECURITY_FLAG_VALID", "LoginIScsiTargetW", "LoginIscsiTarget", "LoginIscsiTarget function [iSCSI Discovery Library API]", "LoginIscsiTargetW", "iscsidisc.loginiscsitarget", "iscsidsc/LoginIscsiTarget", "iscsidsc/LoginIscsiTargetW"]
old-location: iscsidisc\loginiscsitarget.htm
tech.root: iSCSIDisc
ms.assetid: e94e72d2-b93c-41f4-aafc-78e6a97d7a26
ms.date: 12/05/2018
ms.keywords: ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, LoginIScsiTargetW, LoginIscsiTarget, LoginIscsiTarget function [iSCSI Discovery Library API], LoginIscsiTargetA, LoginIscsiTargetW, iscsidisc.loginiscsitarget, iscsidsc/LoginIscsiTarget, iscsidsc/LoginIscsiTargetA, iscsidsc/LoginIscsiTargetW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoginIscsiTargetW (Unicode) and LoginIscsiTargetA (ANSI)
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
 - LoginIScsiTargetW
 - iscsidsc/LoginIScsiTargetW
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
 - LoginIscsiTarget
 - LoginIscsiTargetA
 - LoginIscsiTargetW
---

# LoginIScsiTargetW function


## -description

The <b>LoginIscsiTarget</b> function establishes a full featured login session with the indicated target.

## -parameters

### -param TargetName [in]

The name of the target with which to establish a login session. The target must already exist in the list of discovered targets for the iSCSI initiator service.

### -param IsInformationalSession [in]

If <b>true</b>, the <b>LoginIscsiTarget</b> function establishes a login session, but the operation does not report the LUNs on the target to the "Plug and Play" Manager. If the login succeeds, management applications will be able to query the target for information with the <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsireportluns">SendScsiReportLuns</a> and <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-sendscsireadcapacity">SendScsiReadCapacity</a> functions, but the storage stack will not enumerate the target or load a driver for it. 

If <i>IsInformationalSession</i> is <b>false</b>, <b>LoginIscsiTarget</b> reports the LUNs associated with the target to the "Plug and Play" Manager, and the system loads drivers for the LUNs.

### -param InitiatorInstance [in, optional]

The name of the initiator that logs in to the target. If <i>InitiatorName</i> is <b>null</b>, the iSCSI initiator service selects an initiator.

### -param InitiatorPortNumber [in, optional]

The port number of the Host Bus Adapter (HBA) that initiates the login session. If this parameter is <b>ISCSI_ANY_INITIATOR_PORT</b>, the caller did not specify a port for the initiator HBA to use when logging in to the target. 

If <i>InitiatorName</i> is <b>null</b>, <i>InitiatorPortNumber</i> must be <b>ISCSI_ANY_INITIATOR_PORT</b>.

### -param TargetPortal [in, optional]

Pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a> that indicates the portal that the initiator uses to open the session. The specified portal must belong to a portal group that is associated with the <i>TargetName</i>. If <i>TargetPortal</i> is <b>null</b>, the iSCSI initiator service instructs the initiator to use any portal through which the target is accessible to the initiator. If the caller specifies the value for <i>TargetPortal</i>, the iSCSI initiator service will not verify that the <i>TargetPortal</i> is accessible to the initiator HBA.

### -param SecurityFlags [in, optional]

A bitmap that specifies the characteristics of the IPsec connection that the initiator adds to the session. If an IPsec security policy between the initiator and the target portal is already configured as a result of the current portal group policy or a previous connection to the target, the existing configuration takes precedence over the configuration specified in <i>SecurityFlags</i>. 

If the ISCSI_SECURITY_FLAG_VALID flag is set to 0, the iSCSI initiator service uses default values for the security flags that are defined in the registry. 

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

### -param Mappings [in, optional]

An array of structures of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a>, each of which holds information that the initiator uses to assign bus, target and LUN numbers to the devices that are associated with the target. If <i>Mappings</i> is <b>null</b>, the initiator will select the bus, target and LUN numbers.

### -param LoginOptions [in, optional]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a> that contains the options that specify the characteristics of the login session.

### -param KeySize [in, optional]

The size, in bytes, of the target's preshared key specified by the <i>Key</i> parameter.

### -param Key [in, optional]

A preshared key to use when logging in to the target portal that exposes this target. 

<div class="alert"><b>Note</b>  If an IPsec policy is already associated with the target portal, the IPsec settings in this call are ignored.</div>
<div> </div>

### -param IsPersistent [in]

If <b>true</b>, the initiator should save the characteristics of the login session in non-volatile storage, so that the information persists across restarts of the initiator device and reboots of the operating system. The initiator should not establish the login session until after saving the persistent data. 

Whenever the initiator device restarts, it should automatically attempt to re-establish the login session with the same characteristics. If <b>false</b>, the initiator device simply logs in to the target without saving the characteristics of the login session.

### -param UniqueSessionId [out]

A pointer to a structure of type <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> that, on return, contains a unique session identifier for the login session.

### -param UniqueConnectionId [out]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/legacy/bb870817(v=vs.85)">ISCSI_UNIQUE_CONNECTION_ID</a> that, on return, contains a unique connection identifier for the login session.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -remarks

The <b>LoginIscsiTarget</b> function either establishes a single login session with a target, or creates a persistent login to a target. If <b>LoginIscsiTarget</b> creates a persistent login, the specified initiator should log in to the target each time the initiator is started, typically at system boot. Callers to <b>LoginIscsiTarget</b> can request the creation of a persistent login by setting the <i>IsPersistent</i> parameter to <b>true</b>.





> [!NOTE]
> The iscsidsc.h header defines LoginIScsiTarget as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a>



<a href="/previous-versions/windows/desktop/legacy/bb870817(v=vs.85)">ISCSI_UNIQUE_CONNECTION_ID</a>



<a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>
