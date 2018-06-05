---
UID: NS:wincrypt._CERT_NAME_VALUE
title: "_CERT_NAME_VALUE"
author: windows-sdk-content
description: Contains a relative distinguished name (RDN) attribute value.
old-location: security\cert_name_value.htm
old-project: SecCrypto
ms.assetid: 9f4ba546-7881-4827-b8f5-c3dd8c54ea8b
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCERT_NAME_VALUE, CERT_NAME_VALUE, CERT_NAME_VALUE structure [Security], PCERT_NAME_VALUE, PCERT_NAME_VALUE structure pointer [Security], _CERT_NAME_VALUE, _crypto2_cert_name_value, security.cert_name_value, wincrypt/CERT_NAME_VALUE, wincrypt/PCERT_NAME_VALUE"
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
req.typenames: CERT_NAME_VALUE, *PCERT_NAME_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_NAME_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_NAME_VALUE structure


## -description


The <b>CERT_NAME_VALUE</b> structure contains a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">relative distinguished name</a> (RDN) attribute value. It is like the 
<a href="https://msdn.microsoft.com/4729e824-761c-4115-8b7b-76ffdab8ea62">CERT_RDN_ATTR</a> structure, except that it does not include the object identifier member that is a member of <b>CERT_RDN_ATTR</b>. As in <b>CERT_RDN_ATTR</b>, the interpretation of the <b>Value</b> member depends on <b>dwValueType</b>.


## -struct-fields




### -field dwValueType

Indicates the interpretation of the <b>Value</b> member. For documentation on possible values of <b>dwValueType</b>, see 
<a href="https://msdn.microsoft.com/4729e824-761c-4115-8b7b-76ffdab8ea62">CERT_RDN_ATTR</a>.


### -field Value


<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the RDN attribute. The <b>cbData</b> member of <b>Value</b> is the length, in bytes, of the <b>pbData</b> member. It is not the number of elements in the <b>pbData</b> string. 




For example, a <b>DWORD</b> is 32 bits or 4 bytes long. If the <b>pbData</b> member of <b>Value</b> is a <b>DWORD</b> array, the <b>cbData</b> member of <b>Value</b> would be four times the number of <b>DWORD</b> elements in the array. A <b>short</b> data type is 16 bits or 2 bytes long. If the <b>pbData</b> member is an array of <b>short</b> data types, the <b>cbData</b> member must be two times the length of the array.

The <b>pbData</b> member of <b>Value</b> can be a null-terminated array of 8-bit or 16-bit characters or a fixed-length array of elements. If <b>dwValueType</b> is set to CERT_RDN_ENCODED_BLOB, <b>pbData</b> is encoded.


## -see-also




<a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a>



<a href="https://msdn.microsoft.com/4729e824-761c-4115-8b7b-76ffdab8ea62">CERT_RDN_ATTR</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/c1e0af19-320e-411e-85bf-c7f01befcac4">CertRDNValueToStr</a>
 

 

