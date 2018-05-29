---
UID: NS:webservices._WS_THUMBPRINT_CERT_CREDENTIAL
title: "_WS_THUMBPRINT_CERT_CREDENTIAL"
author: windows-sdk-content
description: The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.
old-location: wsw\ws_thumbprint_cert_credential.htm
old-project: wsw
ms.assetid: b1e7b6a6-1f71-4bcd-9c0e-9a46b963b19b
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_THUMBPRINT_CERT_CREDENTIAL, WS_THUMBPRINT_CERT_CREDENTIAL structure [Web Services for Windows], _WS_THUMBPRINT_CERT_CREDENTIAL, webservices/WS_THUMBPRINT_CERT_CREDENTIAL, wsw.ws_thumbprint_cert_credential
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: WS_THUMBPRINT_CERT_CREDENTIAL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_THUMBPRINT_CERT_CREDENTIAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_THUMBPRINT_CERT_CREDENTIAL structure


## -description



The type for specifying a certificate credential using the
certificate's thumbprint, store location and store name.  The
specified credential is loaded when the containing channel or listener
is opened.
            


The thumbprint is the best option for specifying a certificate when
subject name based specification is expected to be ambiguous due to
the presence of multiple certificates with matching subject names in
the cert store being specified.
            


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
                


### -field thumbprint


The SHA-1 thumbprint (such as
"c0f89c8d4e4e80f250b58c3fae944a0edee02804") of the specified
certificate.  The supplied value should be a hexadecimal string
without whitespace characters or a leading 0x.  A tool such as
certmgr.exe may be used to find the thumbprint of a certificate.
                

