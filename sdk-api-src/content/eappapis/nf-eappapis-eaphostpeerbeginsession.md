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

# EapHostPeerBeginSession function


## -description


Starts an EAP authentication session. 
 If the <b>EapHostPeerBeginSession</b> function succeeds, the caller must also call <a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a> to end the authentication session. The latter function must be called regardless of whether functions other than <b>EapHostPeerBeginSession</b> succeed or fail.    

If re-authentication is required, regardless of the reason, the interface represented by the parameter <i>pConnectionId</i> will be unregistered. In cases where <i>pConnectionId</i> is unregistered, you must also call <a href="https://msdn.microsoft.com/1d997e4e-6e7f-47db-9957-9658e54c0bdf">EapHostPeerClearConnection</a> to remove the connection.

Never call  <b>EapHostPeerBeginSession</b> again on an interface without calling <a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>. Only one  authentication session can be active on the interface specified by <i>pConnectionId</i>.


## -parameters




### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  new EAP authentication session behavior.


### -param eapType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that specifies the type of EAP authentication to use for this session.


### -param pAttributeArray [in]

Pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> structure that specifies the EAP attributes of the entity to authenticate.


### -param hTokenImpersonateUser [in]

Handle to the user impersonation token to use in this session.


### -param dwSizeofConnectionData

TBD


### -param pConnectionData [in]

Describes the configuration used for authentication. <b>NULL</b> connection data is considered valid. The method should work with the default configuration.
 


### -param dwSizeofUserData

TBD


### -param pUserData [in]

A pointer to a byte buffer that contains the opaque user data BLOB containing user data returned from the <a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a> function.  User data may include credentials or certificates used for authentication. <i>pUserData</i> can be <b>NULL</b>. The interpretation of a <b>NULL</b> pointer depends on the implementation of a method. The user data consists of user or machine credentials used for authentication. Typically the user data depends on the configuration data.

If <b>EAP_FLAG_PREFER_ALT_CREDENTIALS</b> is indicated in <i>dwflags</i>, then credentials passed into <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a> are preferred to all other forms of credential retrieval, even if configuration  data passed into <i>pConnectionData</i> requests a different mode of credential retrieval. If passing credentials into <b>EapPeerBeginSession</b> fails, then EAPHost resorts to method specific credential retrieval, in which case credentials could be obtained from a file, Windows login, or a certificate store, for example.

The EAP method author defines both the default credentials and alternate credentials. For example, in the case of EAP-MSCHAPv2 the default credentials are Windows credentials obtained from winlogon, and  alternate credentials are the credentials (user name, password, domain) passed into  <i>pUserData</i>.


### -param dwMaxSendPacketSize [in]

The maximum size, in bytes, of an EAP packet that can be sent during the session.


### -param pConnectionId [in]

A pointer to a GUID value that uniquely identifies the logical network interface over which the authentication of the supplicant will take place. If the supplicant seeks re-authentication after a NAP health change, it should provide a unique GUID.
   The parameter should be <b>NULL</b> when this function is called by a tunneling method to start its inner method.   When the <i>pConnectionId</i> parameter is <b>NULL</b>, the <i>func</i> and <i>pContextData</i> parameters are ignored. 


### -param func [in]

A <a href="https://msdn.microsoft.com/7fa12cb4-694a-4db6-9743-5a2cbb995721">NotificationHandler</a> function pointer that provides the callback used by EAPHost to notify the supplicant when re-authentication is needed. 

If the function handler is <b>NULL</b>, the <i>pContextData</i> parameter is ignored. If the function handler is <b>NULL</b>, it also means that the caller is not interested in SoH change notification
   from the EAP quarantine enforcement client (QEC).

The following code shows a <a href="https://msdn.microsoft.com/7fa12cb4-694a-4db6-9743-5a2cbb995721">NotificationHandler</a> callback call.

<pre class="syntax" xml:space="preserve"><code>func(*pConnectionId, pContextData);</code></pre>

### -param pContextData [in]

A pointer to re-authentication context data that the supplicant will associate with the connection when <i>func</i> is called. This parameter can be <b>NULL</b>. 


### -param pSessionId [out]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>. 


#### - dwSizeOfConnectionData [in]

The size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.


#### - dwSizeOfUserData [in]

The size, in bytes, of the user data buffer provided in <i>pUserData</i>.


## -remarks



If an EAPHost supplicant is participating in NAP, the supplicant will respond to changes in the state of its network health. If that state changes, the supplicant must then initiate a re-authentication session as follows. 

<ul>
<li>If there is a current session when re-authentication occurs, the supplicant should tear down the current session by calling <a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>, and then start a new session by calling <b>EapHostPeerBeginSession</b>.</li>
<li>If there is no current session with re-authentication occurs, or the previous session was already ended by calling <a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>, the supplicant only needs to start a new session by calling <b>EapHostPeerBeginSession</b>.</li>
</ul>
The call to <b>EapHostPeerBeginSession</b> to establish the re-authentication session can be made from the callback specified in the <i>func</i> parameter  and called when the health state changes. This callback function indicates to the supplicant to tear down the network authentication associated with the GUID and re-authenticate.   

A  connection can be kept across multiple sessions because <b>EapHostPeerBeginSession</b> can provide a valid GUID to register the connection. When <a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a> is called, only the current session is terminated. Because the registration with the GUID isn't terminated, the original registration by <b>EapHostPeerBeginSession</b> remains intact. Therefore, the registration is effective across multiple sessions. 

<div class="alert"><b>Note</b>  Registering the connection refers to providing a valid GUID and valid callback function pointer.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/1d997e4e-6e7f-47db-9957-9658e54c0bdf">EapHostPeerClearConnection</a>



<a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

