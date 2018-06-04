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

# _OCSP_BASIC_RESPONSE_INFO structure


## -description


 The <b>OCSP_BASIC_RESPONSE_INFO</b> structure contains a basic <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) response as specified by <a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560</a>. The RFC specifies that a single response can contain a sequence of certificates for which statuses are provided. The  <b>rgResponseEntry</b> member of this structure contains an <a href="https://msdn.microsoft.com/c22f25fd-bbee-45de-9ca0-064b159abb7c">OCSP_BASIC_RESPONSE_ENTRY</a> structure for each certificate in a sequence.


## -struct-fields




### -field dwVersion

A value that indicates the protocol version of the response.



#### OCSP_BASIC_RESPONSE_V1 (0)


### -field dwResponderIdChoice

A value that indicates the type of ID the responder used in this response.



#### OCSP_BASIC_BY_NAME_RESPONDER_ID (1)



#### OCSP_BASIC_BY_KEY_RESPONDER_ID (2)


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ByNameResponderId

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> structure that contains the subject name of the responder signing <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>.


### -field DUMMYUNIONNAME.ByKeyResponderId

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> that contains a hash of the responder signing certificate <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>.


### -field ProducedAt

The date and time at which the response was signed.


### -field cResponseEntry

The number of elements in the <i>rgResponseEntry</i> array.


### -field rgResponseEntry

An array of pointers to <a href="https://msdn.microsoft.com/c22f25fd-bbee-45de-9ca0-064b159abb7c">OCSP_BASIC_RESPONSE_ENTRY</a> structures, each of which contains a certificate status.


### -field cExtension

The number of elements in the <b>rgExtension</b> array.


### -field rgExtension

An array of pointers to <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures, each of which contains additional information about the response.


## -remarks



OCSP responder applications encode this structure and store it in an <a href="https://msdn.microsoft.com/4b88a946-030f-490a-b46a-c42507e1268d">OCSP_BASIC_SIGNED_RESPONSE_INFO</a> <b>ToBeSigned</b> member. Conversely, OCSP client applications decode the <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> structure to obtain this structure.

OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560 Online Certificate Status Protocol</a>
 

 

