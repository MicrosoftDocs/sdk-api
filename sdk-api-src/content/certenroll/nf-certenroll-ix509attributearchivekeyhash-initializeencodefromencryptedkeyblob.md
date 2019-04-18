---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob
title: IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob (certenroll.h)
author: windows-sdk-content
description: Initializes the attribute from an encrypted private key.
old-location: security\ix509attributearchivekeyhash_initializeencodefromencryptedkeyblob_method.htm
tech.root: seccertenroll
ms.assetid: 2101f15f-b71b-4dea-8ec8-2d3c1926ae15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509AttributeArchiveKeyHash interface [Security],InitializeEncodeFromEncryptedKeyBlob method, IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob, IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob, InitializeEncodeFromEncryptedKeyBlob, InitializeEncodeFromEncryptedKeyBlob method [Security], InitializeEncodeFromEncryptedKeyBlob method [Security],IX509AttributeArchiveKeyHash interface, certenroll/IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob, security.ix509attributearchivekeyhash_initializeencodefromencryptedkeyblob_method
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob


## -description


The <b>InitializeEncodeFromEncryptedKeyBlob</b> method initializes the attribute from an encrypted <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. The method computes a SHA-1 <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the private key.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the key.


### -param strEncryptedKeyBlob [in]

A <b>BSTR</b> variable that contains the encrypted key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENCRYPTED_KEY_HASH</b> (1.3.6.1.4.1.311.21.21). For more information, see <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncodeFromEncryptedKeyBlob</b> or <a href="https://msdn.microsoft.com/c8f59fba-c6ce-4e11-bb25-8a6fd23218d1">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a> object. The two methods complement each other. The <b>InitializeEncodeFromEncryptedKeyBlob</b> method enables you to construct an encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="https://msdn.microsoft.com/ff75aaf8-1544-465b-af0d-620ca6984249">EncryptedKeyHashBlob</a> property to retrieve the raw data.




## -see-also




<a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a>
 

 

