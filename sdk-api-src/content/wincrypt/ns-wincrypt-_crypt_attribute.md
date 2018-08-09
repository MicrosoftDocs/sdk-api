---
UID: NS:wincrypt._CRYPT_ATTRIBUTE
title: "_CRYPT_ATTRIBUTE"
author: windows-sdk-content
description: The CRYPT_ATTRIBUTE structure specifies an attribute that has one or more values.
old-location: security\crypt_attribute.htm
old-project: seccrypto
ms.assetid: cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCRYPT_ATTRIBUTE, CRYPT_ATTRIBUTE, CRYPT_ATTRIBUTE structure [Security], PCRYPT_ATTRIBUTE, PCRYPT_ATTRIBUTE structure pointer [Security], _CRYPT_ATTRIBUTE, _crypto2_crypt_attribute, security.crypt_attribute, wincrypt/CRYPT_ATTRIBUTE, wincrypt/PCRYPT_ATTRIBUTE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
tech.root: 
req.typenames: CRYPT_ATTRIBUTE, *PCRYPT_ATTRIBUTE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_ATTRIBUTE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_ATTRIBUTE structure


## -description


The <b>CRYPT_ATTRIBUTE</b> structure specifies an attribute that has one or more values.


## -struct-fields




### -field pszObjId

An <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that specifies the type of data contained in the <b>rgValue</b> array.


### -field cValue

A <b>DWORD</b>  value that indicates the number of elements in the <b>rgValue</b> array.


### -field rgValue

Pointer to an array of <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structures. The <b>cbData</b> member of the <b>CRYPT_INTEGER_BLOB</b> structure indicates the length of the <b>pbData</b> member. The <b>pbData</b> member contains the attribute information.


## -see-also




<a href="https://msdn.microsoft.com/6edeed33-16e1-4295-90e9-769929ab916a">CERT_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/1601d860-6054-4650-a033-ea088655b7e4">CRYPT_SIGN_MESSAGE_PARA</a>



<a href="https://msdn.microsoft.com/876527dd-1ec5-4783-a7ad-20a0e2d2367a">CRYPT_TIME_STAMP_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/99d690fb-ea85-4cb1-9fb0-bdb02e4ac50a">CertFindAttribute</a>
 

 

