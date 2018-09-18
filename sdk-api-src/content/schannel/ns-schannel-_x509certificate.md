---
UID: NS:schannel._X509Certificate
title: "_X509Certificate"
author: windows-sdk-content
description: Represents an X.509 certificate.
old-location: security\x509certificate.htm
tech.root: secauthn
ms.assetid: 5a337f78-e5de-4ea2-9c15-1056d9e9e38c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*PX509Certificate, PX509Certificate, PX509Certificate structure pointer [Security], X509Certificate, X509Certificate structure [Security], _X509Certificate, schannel/PX509Certificate, schannel/X509Certificate, security.x509certificate"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - X509Certificate
product: Windows
targetos: Windows
req.typenames: X509Certificate, *PX509Certificate
req.redist: 
---

# _X509Certificate structure


## -description


The <b>X509Certificate</b> structure represents an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate.


## -struct-fields




### -field Version

The X.509 version number.


### -field SerialNumber

The serial number of the certificate.


### -field SignatureAlgorithm

The ID of the algorithm used to create the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a> for the certificate.


### -field ValidFrom

The beginning of the period of validity for the certificate.


### -field ValidUntil

The end of the period of validity for the certificate.


### -field pszIssuer

A pointer to a string that specifies the issuer of the certificate.


### -field pszSubject

A pointer to a string that specifies the subject of the certificate.


### -field pPublicKey

A pointer to the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> used to create the signature for the certificate.

