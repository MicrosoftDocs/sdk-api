---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorGetInfo
title: EapMethodAuthenticatorGetInfo function (eapmethodauthenticatorapis.h)
description: Obtains a set of function pointers for an implementation of the loaded EAP authenticator method.EapMethodAuthenticatorGetInfo is a function prototype.
helpviewer_keywords: ["EapMethodAuthenticatorGetInfo","EapMethodAuthenticatorGetInfo function [EAPHost]","eaphost.eapmethodauthenticatorgetinfo","eapmethodauthenticatorapis/EapMethodAuthenticatorGetInfo"]
old-location: eaphost\eapmethodauthenticatorgetinfo.htm
tech.root: eaphost
ms.assetid: 83a643bb-5d2e-4227-b82e-e63035860f46
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorGetInfo, EapMethodAuthenticatorGetInfo function [EAPHost], eaphost.eapmethodauthenticatorgetinfo, eapmethodauthenticatorapis/EapMethodAuthenticatorGetInfo
req.header: eapmethodauthenticatorapis.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapMethodAuthenticatorGetInfo
 - eapmethodauthenticatorapis/EapMethodAuthenticatorGetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodauthenticatorapis.h
api_name:
 - EapMethodAuthenticatorGetInfo
---

# EapMethodAuthenticatorGetInfo function


## -description

Obtains a set of function pointers for an implementation of the loaded EAP authenticator method.<b>EapMethodAuthenticatorGetInfo</b> is a function prototype.

## -parameters

### -param pEapType [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains the vendor ID of the EAPHost authenticator function implementer.

### -param pEapInfo [out]

A pointer to an <a href="/windows/win32/api/eapmethodauthenticatorapis/ns-eapmethodauthenticatorapis-eap_authenticator_method_routines">EAP_AUTHENTICATOR_METHOD_ROUTINES</a> structure that contains the function pointers to EAP method-specific implementations of the APIs that correspond to specific RPC calls that can be made by EAP peer method functions.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -remarks

Every EAP authenticator method DLL must have public implementations of the following APIs on it:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinitialize">EapMethodAuthenticatorInitialize</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorupdateinnermethodparams">EapMethodAuthenticatorUpdateInnerMethodParams</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket">EapMethodAuthenticatorReceivePacket</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket">EapMethodAuthenticatorSendPacket</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes">EapMethodAuthenticatorGetAttributes</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes">EapMethodAuthenticatorSetAttributes</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult">EapMethodAuthenticatorGetResult</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession">EapMethodAuthenticatorEndSession</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown">EapMethodAuthenticatorShutdown</a>
</li>
</ul>
These APIs are called on an EAP authenticator method when an authenticator (server) EAPHost receives a specific corresponding RPC call from  a peer (client) EAP method.  Note that a complete one-to-one correspondence does not exist between EAP peer methods and EAP authenticator methods; the specific EAP authenticator method API calls should be made based on the requirements of your implementation of the EAP authenticator method API calls.

This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)