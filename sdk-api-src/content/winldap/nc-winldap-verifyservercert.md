---
UID: NC:winldap.VERIFYSERVERCERT
title: VERIFYSERVERCERT (winldap.h)
description: Allows a client to evaluate the certificate chain of the server to which it is connected.
helpviewer_keywords: ["VERIFYSERVERCERT","VERIFYSERVERCERT callback","VERIFYSERVERCERT callback function [LDAP]","_ldap_verifyservercert","ldap.verifyservercert","winldap/VERIFYSERVERCERT"]
old-location: ldap\verifyservercert.htm
tech.root: ldap
ms.assetid: 3c9993b2-8591-46ff-941b-ff16d42650c9
ms.date: 12/05/2018
ms.keywords: VERIFYSERVERCERT, VERIFYSERVERCERT callback, VERIFYSERVERCERT callback function [LDAP], _ldap_verifyservercert, ldap.verifyservercert, winldap/VERIFYSERVERCERT
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - VERIFYSERVERCERT
 - winldap/VERIFYSERVERCERT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winldap.h
api_name:
 - VERIFYSERVERCERT
---

# VERIFYSERVERCERT callback function


## -description

<b>VERIFYSERVERCERT</b> is a callback function that allows a client to evaluate the certificate chain of the server to which it is connected.

## -parameters

### -param Connection

The session handle.

### -param pServerCert

#### - ppServerCert

A pointer to a pointer to a session handle, represented by <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>.

## -returns

If the function succeeds (the client approves the server certificate), the return value is <b>TRUE</b>.

If the function fails; the return value is <b>FALSE</b> and the secure connection is torn down.

## -remarks

The <b>VERIFYSERVERCERT</b> callback function allows the client to verify the certificate of the server. The client registers a callback which is invoked after the secure connection is set up. The server certificate context is presented to the callback function, where it can be verified as acceptable or not. To register this callback, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a> where CertRoutine is the address of your callback function.


```cpp
conn, LDAP_OPT_SERVER_CERTIFICATE, &CertRoutine
```


The server calls <b>VERIFYSERVERCERT</b> after the secure connection has been established. The server's certificate context is supplied for examination by the client.

An application should use the <i>ppServerCert</i> parameter as: <code>PCCERT_CONTEXT* ppServerCert = (PCCERT_CONTEXT*)pServerCert;</code>

Even though <b>VERIFYSERVERCERT</b> is declared as receiving a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">PCCERT_CONTEXT</a>, it in fact receives a <b>PCCERT_CONTEXT</b>*. The <i>ppServerCert</i> can be used to verify the certificate. <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> should be called before this function returns. The call to this function should be made as follows:


```cpp
CertFreeCertificateContext(*ppServerCert);
```


Or, alternatively, as:


```cpp
CertFreeCertificateContext(*((PCCERT_CONTEXT*)pServerCert));
```

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>
