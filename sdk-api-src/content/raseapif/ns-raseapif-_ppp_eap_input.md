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

# _PPP_EAP_INPUT structure


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
Indicates that this connection is the first link in a multilink connection. See <a href="https://msdn.microsoft.com/a6aee73b-43b2-43b4-a6f1-ac7b293c44ad">Multilink and Callback Connections</a> for more information.

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
<a href="https://msdn.microsoft.com/36659154-de2b-4a94-b25e-b731a4ef9d99">RAS_AUTH_ATTRIBUTE</a> structures. The array is terminated by a structure with an <b>raaType</b> member that has a value of <b>raatMinimum</b> (see 
<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a>). During the 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a> call, this array contains attributes that describe the currently dialed-in user. When the <b>fAuthenticationComplete</b> member is <b>TRUE</b>, this array may contain attributes returned by the authentication provider.


### -field fAuthenticationComplete

Specifies a Boolean value that indicates whether the authentication provider has authenticated the user. A value of <b>TRUE</b> indicates authentication completion. Check the <b>dwAuthResultCode</b> member to determine if the authentication was successful. Ignore this member if the authentication protocol is not using an authentication provider.


### -field dwAuthResultCode

Specifies the result of the authentication provider's authentication process. Successful authentication results in <b>NO_ERROR</b>. Authentication failure codes for <b>dwAuthResultCode</b> must come only from Winerror.h, Raserror.h or Mprerror.h. Ignore this field if the authentication protocol is not using an authentication provider.


### -field hTokenImpersonateUser

Handle to an impersonation token for the user requesting authentication. This member is valid only on the client side. For more information on impersonation tokens, see <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">Access Tokens</a>. 


### -field fSuccessPacketReceived

Specifies that authentication was successful. RAS sets this member to <b>TRUE</b> if the client receives an Network Control Protocol (NCP) packet even though the client has not yet received an EAP success packet. A value of <b>FALSE</b> indicates that no NCP packet has been received.

The EAP success packet is a non-acknowledged packet. Therefore, it may be lost and not resent by the server. In this situation, the receipt of an NCP packet indicates that authentication was successful, since the server has moved on to the NCP phase of PPP.

Examine this member only on the client side.


### -field fDataReceivedFromInteractiveUI

Specifies whether information is available from the interactive user interface. Default is <b>FALSE</b>. RAS sets this member to <b>TRUE</b> whenever the user exits from the authentication protocol's interactive user interface.


### -field pDataFromInteractiveUI

Pointer to data received from the authentication protocol's interactive user interface. This pointer is non-<b>NULL</b> if the <b>fDataReceivedFromInteractiveUI</b> member is <b>TRUE</b> and the interactive user interface did, in fact, return data. Otherwise, this pointer is <b>NULL</b>.

If non-<b>NULL</b>, the authentication protocol should make a copy of the data in its own memory space. RAS frees the memory occupied by this data on return from the call in which the <b>PPP_EAP_INPUT</b> structure was passed. To free the memory, RAS calls the <a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a> function.


### -field dwSizeOfDataFromInteractiveUI

Specifies the size, in bytes, of the data pointed to by <b>pDataFromInteractiveUI</b>. If no data is returned from the interactive user interface, this member is zero.


### -field pConnectionData

Pointer to connection data received from the authentication protocol's configuration user interface. This data is available only when the <b>PPP_EAP_INPUT</b> structure is passed in <a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>. It is not available in calls to <a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>.

The authentication protocol should make a copy of this data in its own memory space. RAS frees the memory occupied by this data on return from the call in which the <b>PPP_EAP_INPUT</b> structure was passed. To free the memory, RAS calls the <a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a> function. 

If the authentication protocol's configuration user interface does not return any data, this member is <b>NULL</b>.


### -field dwSizeOfConnectionData

Specifies the size in bytes of the data pointed to by <b>pConnectionData</b>. If <b>pConnectionData</b> is <b>NULL</b>, this member is zero.


### -field pUserData

Pointer to user data received from the authentication protocol's <a href="https://msdn.microsoft.com/66bc34d2-54b9-46eb-b952-6ad66868c8ce">RasEapGetIdentity</a> function on the client computer. If the authentication protocol does not implement <b>RasEapGetIdentity</b>, this member points to data from the registry for this user.

This data is available only when the <b>PPP_EAP_INPUT</b> structure is passed in <a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>. It is not available in calls to <a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>.

The authentication protocol should make a copy of this data in its own memory space. RAS frees the memory occupied by this data on return from the call in which the <b>PPP_EAP_INPUT</b> structure was passed. 



If the <a href="https://msdn.microsoft.com/66bc34d2-54b9-46eb-b952-6ad66868c8ce">RasEapGetIdentity</a> function is not implemented or did not return any data, and no data exists for the user in the registry, this member is <b>NULL</b>.


### -field dwSizeOfUserData

Specifies the size, in bytes, of the data pointed to by <b>pUserData</b>. If <b>pUserData</b> is <b>NULL</b>, this member is zero.


### -field hReserved

This member is reserved.


### -field guidConnectionId

 


### -field isVpn

 




## -remarks



The <b>PPP_EAP_INPUT</b> structure is passed by RAS to the authentication protocol in calls to 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a> and 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>.

The <b>pwszIdentity</b> and <b>pwszPassword</b> members of the 
<b>PPP_EAP_INPUT</b> structure are used by the 
<b>RasEapBegin</b> function to obtain user information. The <b>pwszPassword</b> member is non-<b>NULL</b> only if the <b>fAuthenticator</b> member is <b>FALSE</b>, that is, the authentication protocol is running on the client computer.

If the authentication protocol is using an authentication provider, such as Radius or Windows 2000 domain authentication, the following members are used to interface with the authentication provider:

<b>pUserAttributes</b>
<b>fAuthenticationComplete</b>
<b>dwAuthResultCode</b>
Note that the array of 
<a href="https://msdn.microsoft.com/36659154-de2b-4a94-b25e-b731a4ef9d99">RAS_AUTH_ATTRIBUTE</a> structures is passed only if <b>fAuthenticator</b> is <b>TRUE</b>. This array contains current session information such as port identifier and local IP address.




## -see-also




<a href="https://msdn.microsoft.com/f2f1cf75-18d4-4764-a747-24662f166eb7">EAP Structures</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/36659154-de2b-4a94-b25e-b731a4ef9d99">RAS_AUTH_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>



<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a>



<a href="https://msdn.microsoft.com/66bc34d2-54b9-46eb-b952-6ad66868c8ce">RasEapGetIdentity</a>



<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>
 

 

