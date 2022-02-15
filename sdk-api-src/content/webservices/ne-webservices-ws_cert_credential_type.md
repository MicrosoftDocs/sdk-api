---
UID: NE:webservices.__unnamed_enum_70
title: WS_CERT_CREDENTIAL_TYPE (webservices.h)
description: The type of the certificate credential, used as a selector for subtypes of WS_CERT_CREDENTIAL.
helpviewer_keywords: ["WS_CERT_CREDENTIAL_TYPE","WS_CERT_CREDENTIAL_TYPE enumeration [Web Services for Windows]","WS_CUSTOM_CERT_CREDENTIAL_TYPE","WS_SUBJECT_NAME_CERT_CREDENTIAL_TYPE","WS_THUMBPRINT_CERT_CREDENTIAL_TYPE","webservices/WS_CERT_CREDENTIAL_TYPE","webservices/WS_CUSTOM_CERT_CREDENTIAL_TYPE","webservices/WS_SUBJECT_NAME_CERT_CREDENTIAL_TYPE","webservices/WS_THUMBPRINT_CERT_CREDENTIAL_TYPE","wsw.ws_cert_credential_type"]
old-location: wsw\ws_cert_credential_type.htm
tech.root: wsw
ms.assetid: 8a14636a-1ec6-4d69-8fd9-bb67e80c73b1
ms.date: 12/05/2018
ms.keywords: WS_CERT_CREDENTIAL_TYPE, WS_CERT_CREDENTIAL_TYPE enumeration [Web Services for Windows], WS_CUSTOM_CERT_CREDENTIAL_TYPE, WS_SUBJECT_NAME_CERT_CREDENTIAL_TYPE, WS_THUMBPRINT_CERT_CREDENTIAL_TYPE, webservices/WS_CERT_CREDENTIAL_TYPE, webservices/WS_CUSTOM_CERT_CREDENTIAL_TYPE, webservices/WS_SUBJECT_NAME_CERT_CREDENTIAL_TYPE, webservices/WS_THUMBPRINT_CERT_CREDENTIAL_TYPE, wsw.ws_cert_credential_type
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
req.typenames: WS_CERT_CREDENTIAL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CERT_CREDENTIAL_TYPE
 - webservices/WS_CERT_CREDENTIAL_TYPE
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
 - WS_CERT_CREDENTIAL_TYPE
---

# WS_CERT_CREDENTIAL_TYPE enumeration


## -description

The type of the certificate credential, used as a selector for
subtypes of <a href="/windows/desktop/api/webservices/ns-webservices-ws_cert_credential">WS_CERT_CREDENTIAL</a>.

## -enum-fields

### -field WS_SUBJECT_NAME_CERT_CREDENTIAL_TYPE:1

Type id for the certificate credential <a href="/windows/win32/api/webservices/ns-webservices-ws_subject_name_cert_credential">WS_SUBJECT_NAME_CERT_CREDENTIAL</a>.

### -field WS_THUMBPRINT_CERT_CREDENTIAL_TYPE:2

Type id for the certificate credential <a href="/windows/win32/api/webservices/ns-webservices-ws_thumbprint_cert_credential">WS_THUMBPRINT_CERT_CREDENTIAL</a>.

### -field WS_CUSTOM_CERT_CREDENTIAL_TYPE:3

Type id for the certificate credential <a href="/windows/desktop/api/webservices/ns-webservices-ws_custom_cert_credential">WS_CUSTOM_CERT_CREDENTIAL</a>.
