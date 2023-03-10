---
UID: NF:eapmethodpeerapis.EapPeerSetCredentials
title: EapPeerSetCredentials function (eapmethodpeerapis.h)
description: Supplies new or updated authentication credentials to the EAP method.
helpviewer_keywords: ["EapPeerSetCredentials","EapPeerSetCredentials function [EAPHost]","eaphost.eappeersetcredentials","eapmethodpeerapis/EapPeerSetCredentials"]
old-location: eaphost\eappeersetcredentials.htm
tech.root: eaphost
ms.assetid: d50a72bd-0b3f-4b68-be96-5debb3fd99f8
ms.date: 12/05/2018
ms.keywords: EapPeerSetCredentials, EapPeerSetCredentials function [EAPHost], eaphost.eappeersetcredentials, eapmethodpeerapis/EapPeerSetCredentials
req.header: eapmethodpeerapis.h
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
 - EapPeerSetCredentials
 - eapmethodpeerapis/EapPeerSetCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerSetCredentials
---

# EapPeerSetCredentials function


## -description

Supplies new or updated authentication credentials to the EAP method.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param pwszIdentity [in]

A pointer that specifies the user identity for which to set the credentials. This user identity string is obtained by calling the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a> function.

### -param pwszPassword [in]

A pointer that contains the clear text password for the user identity.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

If the registry key <b>InvokeUserNameDlg</b>  is set, <i>EapPeerSetCredentials</i> should be exported. If the registry key <b>InvokeUserNameDlg</b>  is not set, <i>EapPeerSetCredentials</i> should export the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a> and <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui">EapPeerInvokeIdentityUI</a> functions.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui">EapPeerInvokeIdentityUI</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials">EapPeerSetCredentials</a>