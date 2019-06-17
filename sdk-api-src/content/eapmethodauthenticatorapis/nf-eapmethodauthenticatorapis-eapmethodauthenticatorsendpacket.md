---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorSendPacket
title: EapMethodAuthenticatorSendPacket function (eapmethodauthenticatorapis.h)
author: windows-sdk-content
description: Obtains an authentication packet from the EAP authenticator method to send to the supplicant.
old-location: eaphost\eapmethodauthenticatorsendpacket.htm
tech.root: eaphost
ms.assetid: 5227ff56-8ac3-4fd7-b6c0-c2d3ef6b906e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorSendPacket, EapMethodAuthenticatorSendPacket function [EAPHost], eaphost.eapmethodauthenticatorsendpacket, eapmethodauthenticatorapis/EapMethodAuthenticatorSendPacket
ms.topic: function
f1_keywords: ["eapmethodauthenticatorapis/EapMethodAuthenticatorSendPacket"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodauthenticatorapis.h
api_name:
 - EapMethodAuthenticatorSendPacket
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapMethodAuthenticatorSendPacket function


## -description


Obtains an authentication packet from the EAP authenticator method to send to the supplicant.

<b>EapMethodAuthenticatorSendPacket</b> is a function prototype. 


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>.


### -param bPacketId [in]

Specifies a numeric ID value for the packet to send.


### -param pcbSendPacket [in, out]

Specifies the maximum size, in bytes, of the packet to send. On return, this parameter receives the size, in bytes, of the packet returned in <i>pEapPacket</i>.


### -param pSendPacket [out]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-tageappacket">EapPacket</a> structure that contains the packet to send to the supplicant.


### -param pTimeout [out]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapauthenticatortypes/ne-eapauthenticatortypes-_eap_authenticator_send_timeout">EAP_AUTHENTICATOR_SEND_TIMEOUT</a> enumeration that specifies the timeout for the packet.


### -param ppEapError [out]

A pointer to the address of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-authenticator-method-functions">EAPHost Authenticator Method Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>
 

 

