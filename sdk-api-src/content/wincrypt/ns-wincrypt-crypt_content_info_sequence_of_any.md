---
UID: NS:wincrypt._CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
title: CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY (wincrypt.h)
author: windows-sdk-content
description: Contains information representing the Netscape certificate sequence of certificates.
old-location: security\crypt_content_info_sequence_of_any.htm
tech.root: SecCrypto
ms.assetid: b47cc15d-b92d-4e8a-a8b8-6217d07a0495
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure [Security], PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure pointer [Security], _crypto2_crypt_content_info_sequence_of_any, security.crypt_content_info_sequence_of_any, wincrypt/CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, wincrypt/PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
product: Windows
targetos: Windows
req.typenames: CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, *PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
req.redist: 
---

# CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure


## -description


The <b>CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY</b> structure contains information representing the Netscape certificate sequence of certificates.

A Netscape certificate sequence of certificates can be created by setting the <b>pszObjId</b> member to szOID_NETSCAPE_CERT_SEQUENCE and supplying <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">DER</a>-encoded certificates in <b>rgValue</b>.


## -struct-fields




### -field pszObjId

Object identifier (OID) specifying the type of data contained in the <b>rgValue</b> array.


### -field cValue

Number of elements in the <b>rgValue</b> array.


### -field rgValue

Array of pointers to <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structures. For more information, see 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>.

