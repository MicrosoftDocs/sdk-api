---
UID: NS:iscsidsc.ISCSI_LOGIN_OPTIONS
title: ISCSI_LOGIN_OPTIONS (iscsidsc.h)
description: ISCSI_LOGIN_OPTIONS structure is used by initiators to specify the characteristics of a login session.
helpviewer_keywords: ["*PISCSI_LOGIN_OPTIONS","ISCSI_LOGIN_FLAG_ALLOW_PORTAL_HOPPING","ISCSI_LOGIN_FLAG_MULTIPATH_ENABLED","ISCSI_LOGIN_FLAG_REQUIRE_IPSEC","ISCSI_LOGIN_FLAG_RESERVED1","ISCSI_LOGIN_OPTIONS","ISCSI_LOGIN_OPTIONS structure [iSCSI Discovery Library API]","ISCSI_LOGIN_OPTIONS_AUTH_TYPE","ISCSI_LOGIN_OPTIONS_DATA_DIGEST","ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_RETAIN","ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_WAIT","ISCSI_LOGIN_OPTIONS_HEADER_DIGEST","ISCSI_LOGIN_OPTIONS_MAXIMUM_CONNECTIONS","ISCSI_LOGIN_OPTIONS_PASSWORD","ISCSI_LOGIN_OPTIONS_USERNAME","PISCSI_LOGIN_OPTIONS","PISCSI_LOGIN_OPTIONS structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_login_options","iscsidsc/ISCSI_LOGIN_OPTIONS","iscsidsc/PISCSI_LOGIN_OPTIONS"]
old-location: iscsidisc\iscsi_login_options.htm
tech.root: iSCSIDisc
ms.assetid: 7d45be86-3d85-4253-aef7-92e05379f1b2
ms.date: 12/05/2018
ms.keywords: '*PISCSI_LOGIN_OPTIONS, ISCSI_LOGIN_FLAG_ALLOW_PORTAL_HOPPING, ISCSI_LOGIN_FLAG_MULTIPATH_ENABLED, ISCSI_LOGIN_FLAG_REQUIRE_IPSEC, ISCSI_LOGIN_FLAG_RESERVED1, ISCSI_LOGIN_OPTIONS, ISCSI_LOGIN_OPTIONS structure [iSCSI Discovery Library API], ISCSI_LOGIN_OPTIONS_AUTH_TYPE, ISCSI_LOGIN_OPTIONS_DATA_DIGEST, ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_RETAIN, ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_WAIT, ISCSI_LOGIN_OPTIONS_HEADER_DIGEST, ISCSI_LOGIN_OPTIONS_MAXIMUM_CONNECTIONS, ISCSI_LOGIN_OPTIONS_PASSWORD, ISCSI_LOGIN_OPTIONS_USERNAME, PISCSI_LOGIN_OPTIONS, PISCSI_LOGIN_OPTIONS structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_login_options, iscsidsc/ISCSI_LOGIN_OPTIONS, iscsidsc/PISCSI_LOGIN_OPTIONS'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ISCSI_LOGIN_OPTIONS, *PISCSI_LOGIN_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_LOGIN_OPTIONS
 - iscsidsc/PISCSI_LOGIN_OPTIONS
 - ISCSI_LOGIN_OPTIONS
 - iscsidsc/ISCSI_LOGIN_OPTIONS
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
 - ISCSI_LOGIN_OPTIONS
---

# ISCSI_LOGIN_OPTIONS structure


## -description

The <b>ISCSI_LOGIN_OPTIONS</b> structure is used by initiators to specify the characteristics of a login session.

## -struct-fields

### -field Version

The version of login option definitions that define the data in the structure. This member must be set to ISCSI_LOGIN_OPTIONS_VERSION 0.

### -field InformationSpecified

A bitmap that indicates which parts of the <b>ISCSI_LOGIN_OPTIONS</b> structure contain valid data.

<table>
<tr>
<th>Bit</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_USERNAME"></a><a id="iscsi_login_options_username"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_USERNAME</b></dt>
</dl>
</td>
<td width="60%">
 Specifies a user name to use in making a login connection. 

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_PASSWORD"></a><a id="iscsi_login_options_password"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
Specifies a password to use in making a login connection.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_HEADER_DIGEST"></a><a id="iscsi_login_options_header_digest"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_HEADER_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
Specifies the type of digest in use for guaranteeing the integrity of header data. 

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_DATA_DIGEST"></a><a id="iscsi_login_options_data_digest"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_DATA_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
Specifies the type of digest in use for guaranteeing the integrity of header data.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_MAXIMUM_CONNECTIONS"></a><a id="iscsi_login_options_maximum_connections"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_MAXIMUM_CONNECTIONS</b></dt>
</dl>
</td>
<td width="60%">
Specifies the maximum number of connections to target devices associated with the login session. 

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_WAIT"></a><a id="iscsi_login_options_default_time_2_wait"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_WAIT</b></dt>
</dl>
</td>
<td width="60%">
Specifies the minimum time to wait, in seconds, before attempting to reconnect or reassign a connection that was dropped. 

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_RETAIN"></a><a id="iscsi_login_options_default_time_2_retain"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_DEFAULT_TIME_2_RETAIN</b></dt>
</dl>
</td>
<td width="60%">
Specifies the maximum time allowed to reassign commands after the initial wait indicated in <b>DefaultTime2Wait</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_OPTIONS_AUTH_TYPE"></a><a id="iscsi_login_options_auth_type"></a><dl>
<dt><b>ISCSI_LOGIN_OPTIONS_AUTH_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the type of authentication that establishes the login session. 

</td>
</tr>
</table>

### -field LoginFlags

A bitwise OR of login flags that define certain characteristics of the login session. The following table indicates the values that can be assigned to this member:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_FLAG_RESERVED1"></a><a id="iscsi_login_flag_reserved1"></a><dl>
<dt><b>ISCSI_LOGIN_FLAG_RESERVED1</b></dt>
</dl>
</td>
<td width="60%">
Reserved for internal use.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_FLAG_ALLOW_PORTAL_HOPPING"></a><a id="iscsi_login_flag_allow_portal_hopping"></a><dl>
<dt><b>ISCSI_LOGIN_FLAG_ALLOW_PORTAL_HOPPING</b></dt>
</dl>
</td>
<td width="60%">
The RADIUS server is permitted to use the portal hopping function for a target if configured to do so.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_FLAG_REQUIRE_IPSEC"></a><a id="iscsi_login_flag_require_ipsec"></a><dl>
<dt><b>ISCSI_LOGIN_FLAG_REQUIRE_IPSEC</b></dt>
</dl>
</td>
<td width="60%">
The login session must use the IPsec protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_LOGIN_FLAG_MULTIPATH_ENABLED"></a><a id="iscsi_login_flag_multipath_enabled"></a><dl>
<dt><b>ISCSI_LOGIN_FLAG_MULTIPATH_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
Multipathing is allowed. When specified the iSCSI Initiator service will allow multiple sessions to the same target. If there are multiple sessions to the same target then there must be some sort of multipathing software installed otherwise data corruption will occur on the target. 

</td>
</tr>
</table>

### -field AuthType

An enumerator value of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ne-iscsidsc-iscsi_auth_types">ISCSI_AUTH_TYPES</a> that indicates the authentication type.

### -field HeaderDigest

An enumerator value of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ne-iscsidsc-iscsi_digest_types">ISCSI_DIGEST_TYPES</a> that indicates the type of digest for guaranteeing the integrity of header data.

### -field DataDigest

An enumerator value of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ne-iscsidsc-iscsi_digest_types">ISCSI_DIGEST_TYPES</a> that indicates the type of digest for guaranteeing the integrity of non-header data.

### -field MaximumConnections

A value between 1 and 65535 that specifies the maximum number of connections to the target device that can be associated with the login session.

### -field DefaultTime2Wait

The minimum time to wait, in seconds, before attempting to reconnect or reassign a connection that has been dropped.

### -field DefaultTime2Retain

The maximum time allowed to reassign a connection after the initial wait indicated in <b>DefaultTime2Wait</b> has elapsed.

### -field UsernameLength

The length, in bytes, of the user name specified in the <b>Username</b> member.

### -field PasswordLength

The length, in bytes, of the user name specified in the <b>Password</b> member.

### -field Username

The user name to authenticate to establish the login session. This value is not necessarily a string. For more information, see the Remarks section in this document.

### -field size_is

### -field size_is.UsernameLength

### -field Password

The user name to authenticate to establish the login session. This value is not necessarily a string. For more information, see the Remarks section in this document.

### -field size_is.PasswordLength

## -remarks

Initiators use the <b>ISCSI_LOGIN_OPTIONS</b> structure when creating a login session with the <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-loginiscsitargeta">LoginIScsiTarget</a> routine.

The <b>Username</b> and <b>Password</b> members are either strings or binary values that are used for iSCSI authentication. The exact meaning and function of these two values depends on the type of authentication used. For the Challenge Handshake Authentication Protocol (CHAP), the value in the <b>Username</b> member is the CHAP name, and the value in the <b>Password</b> member is the shared secret of the target. If there is no value specified in <b>Username</b>, the initiator node name is used as the CHAP name.

If the authentication protocol requires that these two values be strings, they must be ANSI strings.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-loginiscsitargeta">LoginIScsiTarget</a>

