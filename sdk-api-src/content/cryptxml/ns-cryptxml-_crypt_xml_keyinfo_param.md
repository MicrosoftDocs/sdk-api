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

# _CRYPT_XML_KEYINFO_PARAM structure


## -description


The <b>CRYPT_XML_KEYINFO_PARAM</b> structure is used by the <a href="https://msdn.microsoft.com/38bd365e-bc63-498c-a650-471429f09d37">CryptXmlSign</a> function to specify the members of the <b>KeyInfo</b> element to be encoded.


## -struct-fields




### -field wszId

A pointer to a null-terminated wide character string that contains the <b>Id</b> attribute of the <b>KeyInfo</b> element.


### -field wszKeyName

A pointer to a null-terminated wide character string that contains the value in the <b>KeyName</b> element.


### -field SKI

A <a href="https://msdn.microsoft.com/1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f">CERT_BLOB</a> structure that contains the value of the <b>X509SKI</b> element.


### -field wszSubjectName

A pointer to a null-terminated wide character string that  contains the value of the <b>X509SubjectName</b> element.


### -field cCertificate

The number of elements in the array pointed to by the <b>rgCertificate</b> member.


### -field rgCertificate

A pointer to an array of <a href="https://msdn.microsoft.com/1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f">CERT_BLOB</a> structures that are used to populate the <b>X509Certificate</b> elements.


### -field cCRL

The number of elements in the array pointed to by the <b>rgCRL</b> member.


### -field rgCRL

A pointer to an array of <a href="https://msdn.microsoft.com/1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f">CERT_BLOB</a> structures that are used to populate the <b>X509CRL</b> elements.

