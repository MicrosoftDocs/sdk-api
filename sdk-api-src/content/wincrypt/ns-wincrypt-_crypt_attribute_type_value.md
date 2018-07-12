---
UID: NS:wincrypt._CRYPT_ATTRIBUTE_TYPE_VALUE
title: "_CRYPT_ATTRIBUTE_TYPE_VALUE"
author: windows-sdk-content
description: Contains a single attribute value. The Value member's CRYPT_OBJID_BLOB is encoded.
old-location: security\crypt_attribute_type_value.htm
old-project: seccrypto
ms.assetid: 84057581-d0a9-464a-9399-ba806e37516f
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "*PCRYPT_ATTRIBUTE_TYPE_VALUE, CRYPT_ATTRIBUTE_TYPE_VALUE, CRYPT_ATTRIBUTE_TYPE_VALUE structure [Security], PCRYPT_ATTRIBUTE_TYPE_VALUE, PCRYPT_ATTRIBUTE_TYPE_VALUE structure pointer [Security], _CRYPT_ATTRIBUTE_TYPE_VALUE, _crypto2_crypt_attribute_type_value, security.crypt_attribute_type_value, wincrypt/CRYPT_ATTRIBUTE_TYPE_VALUE, wincrypt/PCRYPT_ATTRIBUTE_TYPE_VALUE"
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
req.typenames: CRYPT_ATTRIBUTE_TYPE_VALUE, *PCRYPT_ATTRIBUTE_TYPE_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_ATTRIBUTE_TYPE_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_ATTRIBUTE_TYPE_VALUE structure


## -description


The <b>CRYPT_ATTRIBUTE_TYPE_VALUE</b> structure contains a single attribute value. The <b>Value</b> member's <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> is encoded.


## -struct-fields




### -field pszObjId

<a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">Object identifier</a> (OID) that specifies the attribute type data contained in the <b>Value</b> BLOB.


### -field Value

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> that contains the encoded attribute. The <b>cbData</b> member of the <b>CRYPT_OBJID_BLOB</b> structure indicates the length of the <b>pbData</b> member. The <b>pbData</b> member contains the attribute information.


## -see-also




<a href="https://msdn.microsoft.com/1353ef56-cae7-43f2-a31f-2bb3b502450e">CERT_ALT_NAME_ENTRY</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

