---
UID: NS:webservices._WS_SUBJECT_NAME_CERT_CREDENTIAL
title: WS_SUBJECT_NAME_CERT_CREDENTIAL (webservices.h)
description: The type for specifying a certificate credential using the certificate's subject name, store location and store name. The specified credential is loaded when the containing channel or listener is opened.
helpviewer_keywords: ["WS_SUBJECT_NAME_CERT_CREDENTIAL","WS_SUBJECT_NAME_CERT_CREDENTIAL structure [Web Services for Windows]","webservices/WS_SUBJECT_NAME_CERT_CREDENTIAL","wsw.ws_subject_name_cert_credential"]
old-location: wsw\ws_subject_name_cert_credential.htm
tech.root: wsw
ms.assetid: d146d12f-4a1a-44b4-9e08-9f660554fcbb
ms.date: 12/05/2018
ms.keywords: WS_SUBJECT_NAME_CERT_CREDENTIAL, WS_SUBJECT_NAME_CERT_CREDENTIAL structure [Web Services for Windows], webservices/WS_SUBJECT_NAME_CERT_CREDENTIAL, wsw.ws_subject_name_cert_credential
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_SUBJECT_NAME_CERT_CREDENTIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SUBJECT_NAME_CERT_CREDENTIAL
 - webservices/_WS_SUBJECT_NAME_CERT_CREDENTIAL
 - WS_SUBJECT_NAME_CERT_CREDENTIAL
 - webservices/WS_SUBJECT_NAME_CERT_CREDENTIAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SUBJECT_NAME_CERT_CREDENTIAL
---

# WS_SUBJECT_NAME_CERT_CREDENTIAL structure


## -description

The type for specifying a certificate credential using the
certificate's subject name, store location and store name.  The
specified credential is loaded when the containing channel or listener
is opened.

## -struct-fields

### -field credential

The base type from which this type and all other certificate credential types derive.

### -field storeLocation

The certificate store location (such as CERT_SYSTEM_STORE_CURRENT_USER
or CERT_SYSTEM_STORE_LOCAL_MACHINE) that contains the specified
certificate.

### -field storeName

The certificate store name (such as "My") that contains the specified
certificate.

### -field subjectName

The subject name (such as "CN=service.com") of the specified
certificate.  The supplied subject name string must be in a format acceptable to
CERT_FIND_SUBJECT_NAME-based
search.
                (See <a href="/windows/win32/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>.)