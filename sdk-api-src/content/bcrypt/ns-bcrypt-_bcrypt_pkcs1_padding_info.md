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

# _BCRYPT_PKCS1_PADDING_INFO structure


## -description


The <b>BCRYPT_PKCS1_PADDING_INFO</b> structure is used to provide options for the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #1</a> padding scheme.


## -struct-fields




### -field pszAlgId

A pointer to a null-terminated Unicode string that identifies the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic algorithm</a> to use to create the padding. This algorithm must be a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithm</a>. When creating a signature, the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that corresponds to this algorithm is added to the <b>DigestInfo</b> element in the signature, and if this member is <b>NULL</b>, then the OID is not added. When verifying a signature, the verification fails if the OID that corresponds to this member is not the same as the OID in the signature. If there is no OID in the signature, then verification fails unless this member is <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/62286f6b-0d57-4691-83fc-2b9a9740af71">BCryptDecrypt</a>



<a href="https://msdn.microsoft.com/69fe4530-4b7c-40db-a85c-f9dc458735e7">BCryptEncrypt</a>



<a href="https://msdn.microsoft.com/f402ea9e-89ae-4ccc-9591-aa2328287c0e">BCryptSignHash</a>



<a href="https://msdn.microsoft.com/95c32056-e444-441c-bbc1-c5ae82aba964">BCryptVerifySignature</a>
 

 

