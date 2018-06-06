---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.InitializeDecode
title: IX509AttributeArchiveKeyHash::InitializeDecode
author: windows-sdk-content
description: Initializes the object from a Distinguished Encoding Rules (DER) encoded byte array that contains a SHA-1 hash of the encrypted private key.
old-location: security\ix509attributearchivekeyhash_initializedecode_method.htm
old-project: SecCertEnroll
ms.assetid: c8f59fba-c6ce-4e11-bb25-8a6fd23218d1
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509AttributeArchiveKeyHash interface [Security],InitializeDecode method, IX509AttributeArchiveKeyHash.InitializeDecode, IX509AttributeArchiveKeyHash::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509AttributeArchiveKeyHash interface, certenroll/IX509AttributeArchiveKeyHash::InitializeDecode, security.ix509attributearchivekeyhash_initializedecode_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeArchiveKeyHash.InitializeDecode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeArchiveKeyHash::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains a SHA-1 <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of  the encrypted <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains hash value.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded attribute.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENCRYPTED_KEY_HASH</b> (1.3.6.1.4.1.311.21.21). For more information, see <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a>.

You can use this method if you have a DER-encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) object that contains the attribute value. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/2101f15f-b71b-4dea-8ec8-2d3c1926ae15">InitializeEncodeFromEncryptedKeyBlob</a> or <b>InitializeDecode</b> before you can use an <a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a> object. The two methods complement each other. The <b>InitializeEncodeFromEncryptedKeyBlob</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="https://msdn.microsoft.com/ff75aaf8-1544-465b-af0d-620ca6984249">EncryptedKeyHashBlob</a> property to retrieve the raw data.




## -see-also




<a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a>
 

 

