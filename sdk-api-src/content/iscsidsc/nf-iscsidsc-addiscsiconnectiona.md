---
UID: NF:iscsidsc.AddIScsiConnectionA
title: AddIScsiConnectionA function (iscsidsc.h)
description: AddIscsiConnection function adds a new iSCSI connection to an existing session. (ANSI)
helpviewer_keywords: ["AddIScsiConnectionA", "AddIscsiConnectionA", "ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED", "ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED", "ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED", "ISCSI_SECURITY_FLAG_PFS_ENABLED", "ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED", "ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED", "ISCSI_SECURITY_FLAG_VALID", "iscsidsc/AddIscsiConnectionA"]
old-location: iscsidisc\addiscsiconnection.htm
tech.root: iSCSIDisc
ms.assetid: 919bf77f-f8e5-4fd2-926d-6fbca60b2fb2
ms.date: 12/05/2018
ms.keywords: AddIScsiConnectionA, AddIscsiConnection, AddIscsiConnection function [iSCSI Discovery Library API], AddIscsiConnectionA, AddIscsiConnectionW, ISCSI_SECURITY_FLAG_AGGRESSIVE_MODE_ENABLED, ISCSI_SECURITY_FLAG_IKE_IPSEC_ENABLED, ISCSI_SECURITY_FLAG_MAIN_MODE_ENABLED, ISCSI_SECURITY_FLAG_PFS_ENABLED, ISCSI_SECURITY_FLAG_TRANSPORT_MODE_PREFERRED, ISCSI_SECURITY_FLAG_TUNNEL_MODE_PREFERRED, ISCSI_SECURITY_FLAG_VALID, iscsidisc.addiscsiconnection, iscsidsc/AddIscsiConnection, iscsidsc/AddIscsiConnectionA, iscsidsc/AddIscsiConnectionW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddIscsiConnectionW (Unicode) and AddIscsiConnectionA (ANSI)
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
 - AddIScsiConnectionA
 - iscsidsc/AddIScsiConnectionA
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
 - AddIscsiConnection
 - AddIscsiConnectionA
 - AddIscsiConnectionW
---

# AddIScsiConnectionA function


## -description

The <b>AddIscsiConnection</b> function adds a new iSCSI connection to an existing session.

## -parameters

### -param UniqueSessionId [in]

A pointer to a structure of type <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> that, on input, contains the session identifier for the session that was added.

### -param Reserved [in]

This member should be <b>null</b> on input.

### -param InitiatorPortNumber [in, optional]

The number of the port on the initiator that the initiator uses to add the connection. A value of <b>ISCSI_ANY_INITIATOR_PORT</b> indicates that the initiator can use any of its ports to add the connection.

### -param TargetPortal [in]

A pointer to an ISCSI_TARGET_PORTAL-type structure that indicates the target portal to use when adding the connection. 

The portal must belong to the same portal group that the initiator used to login to the target, and it must be a portal that the initiator discovered. The iSCSI initiator service does not verify that the target portal meets these requirements.

### -param SecurityFlags [in, optional]

A bitmap that specifies the characteristics of the IPsec connection that the initiator uses to establish the connection. If IPsec security policy between the initiator and the target portal is already configured because of the portal group policy or a previous connection to the portal, the existing configuration takes precedence over the configuration specified in SecurityFlags and the security bitmap is ignored. 

If the <b>ISCSI_SECURITY_FLAG_VALID</b> flag is set to 0, the iSCSI initiator service uses default values for the security flags that are defined in the registry.

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

### -param LoginOptions [in, optional]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a> that contains the options that specify the characteristics of the login session.

### -param KeySize [in, optional]

The size, in bytes, of the preshared key that is passed to the target.

### -param Key [in, optional]

If the IPsec security policy between the initiator and the target portal is already configured as a result of the portal group policy or a previous connection to the portal, the existing key takes precedence over the key currently specified in this member.

### -param ConnectionId [out, optional]

An <a href="/previous-versions/windows/desktop/legacy/bb870817(v=vs.85)">ISCSI_UNIQUE_CONNECTION_ID</a>-type structure that, on output, receives an opaque value that uniquely identifies the connection that was added to the session.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a>



<a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines AddIScsiConnection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
