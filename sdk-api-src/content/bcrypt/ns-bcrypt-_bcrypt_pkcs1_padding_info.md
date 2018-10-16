---
UID: NS:bcrypt._BCRYPT_PKCS1_PADDING_INFO
title: "_BCRYPT_PKCS1_PADDING_INFO"
author: windows-sdk-content
description: Used to provide options for the PKCS #1 padding scheme.
old-location: security\bcrypt_pkcs1_padding_info.htm
tech.root: seccng
ms.assetid: 920fa461-5b7e-4429-972d-e7c83fb62c64
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: BCRYPT_PKCS1_PADDING_INFO, BCRYPT_PKCS1_PADDING_INFO structure [Security], _BCRYPT_PKCS1_PADDING_INFO, bcrypt/BCRYPT_PKCS1_PADDING_INFO, security.bcrypt_pkcs1_padding_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bcrypt.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_PKCS1_PADDING_INFO
product: Windows
targetos: Windows
req.typenames: BCRYPT_PKCS1_PADDING_INFO
req.redist: 
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
 

 

