---
UID: NF:eappapis.EapHostPeerBeginSession
title: EapHostPeerBeginSession function (eappapis.h)
description: Starts an EAP authentication session.
helpviewer_keywords: ["EapHostPeerBeginSession","EapHostPeerBeginSession function [EAPHost]","eaphost.eaphostpeerbeginsession","eappapis/EapHostPeerBeginSession"]
old-location: eaphost\eaphostpeerbeginsession.htm
tech.root: eaphost
ms.assetid: 9dc339bc-ef01-4432-83cb-b4b14a36f18e
ms.date: 12/05/2018
ms.keywords: EapHostPeerBeginSession, EapHostPeerBeginSession function [EAPHost], eaphost.eaphostpeerbeginsession, eappapis/EapHostPeerBeginSession
req.header: eappapis.h
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerBeginSession
 - eappapis/EapHostPeerBeginSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerBeginSession
---

# EapHostPeerBeginSession function


## -description

Starts an EAP authentication session. 
 If the <b>EapHostPeerBeginSession</b> function succeeds, the caller must also call <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a> to end the authentication session. The latter function must be called regardless of whether functions other than <b>EapHostPeerBeginSession</b> succeed or fail.    

If re-authentication is required, regardless of the reason, the interface represented by the parameter <i>pConnectionId</i> will be unregistered. In cases where <i>pConnectionId</i> is unregistered, you must also call <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection">EapHostPeerClearConnection</a> to remove the connection.

Never call  <b>EapHostPeerBeginSession</b> again on an interface without calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>. Only one  authentication session can be active on the interface specified by <i>pConnectionId</i>.

## -parameters

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  new EAP authentication session behavior.

### -param eapType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that specifies the type of EAP authentication to use for this session.

### -param pAttributeArray [in]

Pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> structure that specifies the EAP attributes of the entity to authenticate.

### -param hTokenImpersonateUser [in]

Handle to the user impersonation token to use in this session.

### -param dwSizeofConnectionData [in]

The size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.

### -param pConnectionData [in]

Describes the configuration used for authentication. <b>NULL</b> connection data is considered valid. The method should work with the default configuration.

### -param dwSizeofUserData [in]

The size, in bytes, of the user data buffer provided in <i>pUserData</i>.

### -param pUserData [in]

A pointer to a byte buffer that contains the opaque user data BLOB containing user data returned from the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a> function.  User data may include credentials or certificates used for authentication. <i>pUserData</i> can be <b>NULL</b>. The interpretation of a <b>NULL</b> pointer depends on the implementation of a method. The user data consists of user or machine credentials used for authentication. Typically the user data depends on the configuration data.

If <b>EAP_FLAG_PREFER_ALT_CREDENTIALS</b> is indicated in <i>dwflags</i>, then credentials passed into <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a> are preferred to all other forms of credential retrieval, even if configuration  data passed into <i>pConnectionData</i> requests a different mode of credential retrieval. If passing credentials into <b>EapPeerBeginSession</b> fails, then EAPHost resorts to method specific credential retrieval, in which case credentials could be obtained from a file, Windows login, or a certificate store, for example.

The EAP method author defines both the default credentials and alternate credentials. For example, in the case of EAP-MSCHAPv2 the default credentials are Windows credentials obtained from winlogon, and  alternate credentials are the credentials (user name, password, domain) passed into  <i>pUserData</i>.

### -param dwMaxSendPacketSize [in]

The maximum size, in bytes, of an EAP packet that can be sent during the session.

### -param pConnectionId [in]

A pointer to a GUID value that uniquely identifies the logical network interface over which the authentication of the supplicant will take place. If the supplicant seeks re-authentication after a NAP health change, it should provide a unique GUID.
   The parameter should be <b>NULL</b> when this function is called by a tunneling method to start its inner method.   When the <i>pConnectionId</i> parameter is <b>NULL</b>, the <i>func</i> and <i>pContextData</i> parameters are ignored.

### -param func [in]

A <a href="/windows/desktop/api/eappapis/nc-eappapis-notificationhandler">NotificationHandler</a> function pointer that provides the callback used by EAPHost to notify the supplicant when re-authentication is needed. 

If the function handler is <b>NULL</b>, the <i>pContextData</i> parameter is ignored. If the function handler is <b>NULL</b>, it also means that the caller is not interested in SoH change notification
   from the EAP quarantine enforcement client (QEC).

The following code shows a <a href="/windows/desktop/api/eappapis/nc-eappapis-notificationhandler">NotificationHandler</a> callback call.


``` syntax
func(*pConnectionId, pContextData);
```


### -param pContextData [in]

A pointer to re-authentication context data that the supplicant will associate with the connection when <i>func</i> is called. This parameter can be <b>NULL</b>.

### -param pSessionId [out]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -remarks

If an EAPHost supplicant is participating in NAP, the supplicant will respond to changes in the state of its network health. If that state changes, the supplicant must then initiate a re-authentication session as follows. 

<ul>
<li>If there is a current session when re-authentication occurs, the supplicant should tear down the current session by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>, and then start a new session by calling <b>EapHostPeerBeginSession</b>.</li>
<li>If there is no current session with re-authentication occurs, or the previous session was already ended by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>, the supplicant only needs to start a new session by calling <b>EapHostPeerBeginSession</b>.</li>
</ul>
The call to <b>EapHostPeerBeginSession</b> to establish the re-authentication session can be made from the callback specified in the <i>func</i> parameter  and called when the health state changes. This callback function indicates to the supplicant to tear down the network authentication associated with the GUID and re-authenticate.   

A  connection can be kept across multiple sessions because <b>EapHostPeerBeginSession</b> can provide a valid GUID to register the connection. When <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a> is called, only the current session is terminated. Because the registration with the GUID isn't terminated, the original registration by <b>EapHostPeerBeginSession</b> remains intact. Therefore, the registration is effective across multiple sessions. 

<div class="alert"><b>Note</b>  Registering the connection refers to providing a valid GUID and valid callback function pointer.</div>
<div> </div>

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection">EapHostPeerClearConnection</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)
