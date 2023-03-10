---
UID: NS:raseapif._PPP_EAP_INPUT
title: PPP_EAP_INPUT (raseapif.h)
description: The PPP_EAP_INPUT structure is used in the interaction between the RAS Connection Manager Service PPP implementation and the EAP.
helpviewer_keywords: ["*PPPP_EAP_INPUT","PPPP_EAP_INPUT","PPPP_EAP_INPUT structure pointer [EAP]","PPP_EAP_INPUT","PPP_EAP_INPUT structure [EAP]","RAS_EAP_FLAG_8021X_AUTH","RAS_EAP_FLAG_ALTERNATIVE_USER_DB","RAS_EAP_FLAG_FIRST_LINK","RAS_EAP_FLAG_GUEST_ACCESS","RAS_EAP_FLAG_LOGON","RAS_EAP_FLAG_NON_INTERACTIVE","RAS_EAP_FLAG_PEAP_UPFRONT","RAS_EAP_FLAG_PRE_LOGON","RAS_EAP_FLAG_RESUME_FROM_HIBERNATE","RAS_EAP_FLAG_ROUTER","_eap_ppp_eap_input","eap.ppp_eap_input","raseapif/PPPP_EAP_INPUT","raseapif/PPP_EAP_INPUT"]
old-location: eap\ppp_eap_input.htm
tech.root: EAP
ms.assetid: 80a8f118-323d-4040-91f7-202eeee6d227
ms.date: 12/05/2018
ms.keywords: '*PPPP_EAP_INPUT, PPPP_EAP_INPUT, PPPP_EAP_INPUT structure pointer [EAP], PPP_EAP_INPUT, PPP_EAP_INPUT structure [EAP], RAS_EAP_FLAG_8021X_AUTH, RAS_EAP_FLAG_ALTERNATIVE_USER_DB, RAS_EAP_FLAG_FIRST_LINK, RAS_EAP_FLAG_GUEST_ACCESS, RAS_EAP_FLAG_LOGON, RAS_EAP_FLAG_NON_INTERACTIVE, RAS_EAP_FLAG_PEAP_UPFRONT, RAS_EAP_FLAG_PRE_LOGON, RAS_EAP_FLAG_RESUME_FROM_HIBERNATE, RAS_EAP_FLAG_ROUTER, _eap_ppp_eap_input, eap.ppp_eap_input, raseapif/PPPP_EAP_INPUT, raseapif/PPP_EAP_INPUT'
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PPP_EAP_INPUT, *PPPP_EAP_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_EAP_INPUT
 - raseapif/_PPP_EAP_INPUT
 - PPPP_EAP_INPUT
 - raseapif/PPPP_EAP_INPUT
 - PPP_EAP_INPUT
 - raseapif/PPP_EAP_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Raseapif.h
api_name:
 - PPP_EAP_INPUT
---

# PPP_EAP_INPUT structure


## -description

The 
<b>PPP_EAP_INPUT</b> structure is used in the interaction between the RAS Connection Manager Service PPP implementation and the EAP.

This structure provides user information, and facilitates the use of authentication providers, such as a RADIUS server.

## -struct-fields

### -field dwSizeInBytes

Specifies the size in bytes of the <b>PPP_EAP_INPUT</b> structure. The value of this member can be used to distinguish between current and future versions of this structure.

### -field fFlags

Specifies zero or more of the following flags that qualify the authentication process.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_ROUTER"></a><a id="ras_eap_flag_router"></a><dl>
<dt><b>RAS_EAP_FLAG_ROUTER</b></dt>
</dl>
</td>
<td width="60%">
Specifies whether the computer dialing in is a router or a RAS client. If the computer is a router, this parameter should be set. 

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_NON_INTERACTIVE"></a><a id="ras_eap_flag_non_interactive"></a><dl>
<dt><b>RAS_EAP_FLAG_NON_INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the authentication protocol should not bring up a user-interface. If the authentication protocol is not able to determine the identity from the data supplied, it should return the error code <b>ERROR_INTERACTIVE_MODE</b>, which is defined in raserror.h.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_LOGON"></a><a id="ras_eap_flag_logon"></a><dl>
<dt><b>RAS_EAP_FLAG_LOGON</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the user data from obtained from Winlogon.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_FIRST_LINK"></a><a id="ras_eap_flag_first_link"></a><dl>
<dt><b>RAS_EAP_FLAG_FIRST_LINK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this connection is the first link in a multilink connection. See [Multilink and Callback Connections](/windows/win32/eap/multilink-and-callback-connections) for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_GUEST_ACCESS"></a><a id="ras_eap_flag_guest_access"></a><dl>
<dt><b>RAS_EAP_FLAG_GUEST_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Specified if the client wants guest access. This flag is normally used in the case of a wireless connection such that if the authentication fails for N number of consecutive tries the wireless client, if configured to request guest access, then does so by passing this flag. The RADIUS server should be setup to permit guest access.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_8021X_AUTH"></a><a id="ras_eap_flag_8021x_auth"></a><dl>
<dt><b>RAS_EAP_FLAG_8021X_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this session is executing in a wireless context.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_RESUME_FROM_HIBERNATE"></a><a id="ras_eap_flag_resume_from_hibernate"></a><dl>
<dt><b>RAS_EAP_FLAG_RESUME_FROM_HIBERNATE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this is the first call after the machine has  resumed from hibernation.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_PEAP_UPFRONT"></a><a id="ras_eap_flag_peap_upfront"></a><dl>
<dt><b>RAS_EAP_FLAG_PEAP_UPFRONT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that PEAP is enabled
                                                        at the beginning of the IAS pipeline.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_ALTERNATIVE_USER_DB"></a><a id="ras_eap_flag_alternative_user_db"></a><dl>
<dt><b>RAS_EAP_FLAG_ALTERNATIVE_USER_DB</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the user database is not Active Directory.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_PRE_LOGON"></a><a id="ras_eap_flag_pre_logon"></a><dl>
<dt><b>RAS_EAP_FLAG_PRE_LOGON</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the credentials for the user or a computer account should be obtained in  a secure fashion without raising multiple UI instances.

</td>
</tr>
</table>

### -field fAuthenticator

Specifies whether the authentication protocol is operating on the server or client. A value of <b>TRUE</b> indicates that the authentication protocol is operating on the server as the authenticator. A value of <b>FALSE</b> indicates that the authentication protocol is operating on the client as the process to be authenticated.

### -field pwszIdentity

Pointer to a Unicode string that identifies the user requesting authentication. This string is of the form domain\user or machine\user. 




If the authentication protocol is able to derive the user's identity from an additional source, for example a certificate, it should verify that the derived identity matches the value of <b>pwszIdentity</b>.

### -field pwszPassword

Pointer to a Unicode string that contains the user's account password. Available only if <b>fAuthenticator</b> is <b>FALSE</b>. This member may be <b>NULL</b>.

### -field bInitialId

Specifies the identifier of the initial EAP packet sent by the DLL. This value is incremented by one for each subsequent request packet.

### -field pUserAttributes

Pointer to an array of 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ras_auth_attribute">RAS_AUTH_ATTRIBUTE</a> structures. The array is terminated by a structure with an <b>raaType</b> member that has a value of <b>raatMinimum</b> (see 
<a href="/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type">RAS_AUTH_ATTRIBUTE_TYPE</a>). During the 
<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a> call, this array contains attributes that describe the currently dialed-in user. When the <b>fAuthenticationComplete</b> member is <b>TRUE</b>, this array may contain attributes returned by the authentication provider.

### -field fAuthenticationComplete

Specifies a Boolean value that indicates whether the authentication provider has authenticated the user. A value of <b>TRUE</b> indicates authentication completion. Check the <b>dwAuthResultCode</b> member to determine if the authentication was successful. Ignore this member if the authentication protocol is not using an authentication provider.

### -field dwAuthResultCode

Specifies the result of the authentication provider's authentication process. Successful authentication results in <b>NO_ERROR</b>. Authentication failure codes for <b>dwAuthResultCode</b> must come only from Winerror.h, Raserror.h or Mprerror.h. Ignore this field if the authentication protocol is not using an authentication provider.

### -field hTokenImpersonateUser

Handle to an impersonation token for the user requesting authentication. This member is valid only on the client side. For more information on impersonation tokens, see <a href="/windows/desktop/SecAuthZ/access-tokens">Access Tokens</a>.

### -field fSuccessPacketReceived

Specifies that authentication was successful. RAS sets this member to <b>TRUE</b> if the client receives an Network Control Protocol (NCP) packet even though the client has not yet received an EAP success packet. A value of <b>FALSE</b> indicates that no NCP packet has been received.

The EAP success packet is a non-acknowledged packet. Therefore, it may be lost and not resent by the server. In this situation, the receipt of an NCP packet indicates that authentication was successful, since the server has moved on to the NCP phase of PPP.

Examine this member only on the client side.

### -field fDataReceivedFromInteractiveUI

Specifies whether information is available from the interactive user interface. Default is <b>FALSE</b>. RAS sets this member to <b>TRUE</b> whenever the user exits from the authentication protocol's interactive user interface.

### -field pDataFromInteractiveUI

Pointer to data received from the authentication protocol's interactive user interface. This pointer is non-<b>NULL</b> if the <b>fDataReceivedFromInteractiveUI</b> member is <b>TRUE</b> and the interactive user interface did, in fact, return data. Otherwise, this pointer is <b>NULL</b>.

If non-<b>NULL</b>, the authentication protocol should make a copy of the data in its own memory space. RAS frees the memory occupied by this data on return from the call in which the <b>PPP_EAP_INPUT</b> structure was passed. To free the memory, RAS calls the <a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a> function.

### -field dwSizeOfDataFromInteractiveUI

Specifies the size, in bytes, of the data pointed to by <b>pDataFromInteractiveUI</b>. If no data is returned from the interactive user interface, this member is zero.

### -field pConnectionData

Pointer to connection data received from the authentication protocol's configuration user interface. This data is available only when the <b>PPP_EAP_INPUT</b> structure is passed in <a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a>. It is not available in calls to <a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>.

The authentication protocol should make a copy of this data in its own memory space. RAS frees the memory occupied by this data on return from the call in which the <b>PPP_EAP_INPUT</b> structure was passed. To free the memory, RAS calls the <a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a> function. 

If the authentication protocol's configuration user interface does not return any data, this member is <b>NULL</b>.

### -field dwSizeOfConnectionData

Specifies the size in bytes of the data pointed to by <b>pConnectionData</b>. If <b>pConnectionData</b> is <b>NULL</b>, this member is zero.

### -field pUserData

Pointer to user data received from the authentication protocol's <a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a> function on the client computer. If the authentication protocol does not implement <b>RasEapGetIdentity</b>, this member points to data from the registry for this user.

This data is available only when the <b>PPP_EAP_INPUT</b> structure is passed in <a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a>. It is not available in calls to <a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>.

The authentication protocol should make a copy of this data in its own memory space. RAS frees the memory occupied by this data on return from the call in which the <b>PPP_EAP_INPUT</b> structure was passed. 



If the <a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a> function is not implemented or did not return any data, and no data exists for the user in the registry, this member is <b>NULL</b>.

### -field dwSizeOfUserData

Specifies the size, in bytes, of the data pointed to by <b>pUserData</b>. If <b>pUserData</b> is <b>NULL</b>, this member is zero.

### -field hReserved

This member is reserved.

### -field guidConnectionId

### -field isVpn

## -remarks

The <b>PPP_EAP_INPUT</b> structure is passed by RAS to the authentication protocol in calls to 
<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a> and 
<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>.

The <b>pwszIdentity</b> and <b>pwszPassword</b> members of the 
<b>PPP_EAP_INPUT</b> structure are used by the 
<b>RasEapBegin</b> function to obtain user information. The <b>pwszPassword</b> member is non-<b>NULL</b> only if the <b>fAuthenticator</b> member is <b>FALSE</b>, that is, the authentication protocol is running on the client computer.

If the authentication protocol is using an authentication provider, such as Radius or Windows 2000 domain authentication, the following members are used to interface with the authentication provider:

<b>pUserAttributes</b>
<b>fAuthenticationComplete</b>
<b>dwAuthResultCode</b>
Note that the array of 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ras_auth_attribute">RAS_AUTH_ATTRIBUTE</a> structures is passed only if <b>fAuthenticator</b> is <b>TRUE</b>. This array contains current session information such as port identifier and local IP address.

## -see-also

[EAP Structures](/windows/win32/eap/eap-structures)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/windows/desktop/api/raseapif/ns-raseapif-ras_auth_attribute">RAS_AUTH_ATTRIBUTE</a>



<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a>



<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>