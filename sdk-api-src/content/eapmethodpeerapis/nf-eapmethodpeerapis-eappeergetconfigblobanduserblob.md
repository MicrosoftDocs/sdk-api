---
UID: NF:eapmethodpeerapis.EapPeerGetConfigBlobAndUserBlob
title: EapPeerGetConfigBlobAndUserBlob function (eapmethodpeerapis.h)
description: Allows EAP method developers to provide the various connection properties and user properties supported by the method. EAPHost invokes this function to create the connection property and user property of the EAP method.
helpviewer_keywords: ["EapPeerGetConfigBlobAndUserBlob","EapPeerGetConfigBlobAndUserBlob function [EAPHost]","eaphost.eappeergetconfigblobanduserblob","eapmethodpeerapis/EapPeerGetConfigBlobAndUserBlob"]
old-location: eaphost\eappeergetconfigblobanduserblob.htm
tech.root: eaphost
ms.assetid: 81817FAA-20AE-4556-BAA5-0EF2A955B6A3
ms.date: 12/05/2018
ms.keywords: EapPeerGetConfigBlobAndUserBlob, EapPeerGetConfigBlobAndUserBlob function [EAPHost], eaphost.eappeergetconfigblobanduserblob, eapmethodpeerapis/EapPeerGetConfigBlobAndUserBlob
req.header: eapmethodpeerapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Eappcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapPeerGetConfigBlobAndUserBlob
 - eapmethodpeerapis/EapPeerGetConfigBlobAndUserBlob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapPeerGetConfigBlobAndUserBlob
---

# EapPeerGetConfigBlobAndUserBlob function


## -description

The <b>EapPeerGetConfigBlobAndUserBlob</b> method allows EAP method developers to provide the various connection properties and user properties supported by the method. EAPHost invokes this function to create the connection property and user property of the EAP method.

## -parameters

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the EAP authentication session behavior.

### -param eapMethodType [in]

The <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param eapCredential [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential">EapCredential</a> structure that contains the credential type and the appropriate credentials.

### -param pdwConfigBlobSize [out]

Receives a pointer to the size, in bytes, of the <i>ppConfigBlob</i> parameter.

### -param ppConfigBlob [out]

Receives a pointer to a pointer that contains a byte buffer with configured connection data.

### -param pdwUserBlobSize [out]

Receives a pointer to the size, in bytes, of the <i>ppUserBlob</i> parameter.

### -param ppUserBlob [out]

Receives a pointer to a pointer that contains a byte buffer with the methods' user data.

### -param ppEapError [out]

 A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -returns

This function should return <b>ERROR_SUCCESS</b> when it is able to generate the correct connection and user blob. In all other cases, it returns the appropriate windows error.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAP flags](/windows/win32/eaphost/eap-method-flags)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential">EapCredential</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>