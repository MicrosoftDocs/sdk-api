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

