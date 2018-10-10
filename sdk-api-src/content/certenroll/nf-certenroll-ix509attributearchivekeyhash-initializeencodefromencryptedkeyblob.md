---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob
title: IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob
author: windows-sdk-content
description: Initializes the attribute from an encrypted private key.
old-location: security\ix509attributearchivekeyhash_initializeencodefromencryptedkeyblob_method.htm
tech.root: SecCertEnroll
ms.assetid: 2101f15f-b71b-4dea-8ec8-2d3c1926ae15
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509AttributeArchiveKeyHash interface [Security],InitializeEncodeFromEncryptedKeyBlob method, IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob, IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob, InitializeEncodeFromEncryptedKeyBlob, InitializeEncodeFromEncryptedKeyBlob method [Security], InitializeEncodeFromEncryptedKeyBlob method [Security],IX509AttributeArchiveKeyHash interface, certenroll/IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob, security.ix509attributearchivekeyhash_initializeencodefromencryptedkeyblob_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob


## -description


The <b>InitializeEncodeFromEncryptedKeyBlob</b> method initializes the attribute from an encrypted <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>. The method computes a SHA-1 <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hash</a> of the private key.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the key.


### -param strEncryptedKeyBlob [in]

A <b>BSTR</b> variable that contains the encrypted key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENCRYPTED_KEY_HASH</b> (1.3.6.1.4.1.311.21.21). For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncodeFromEncryptedKeyBlob</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa377062(v=VS.85).aspx">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/en-us/library/Aa377060(v=VS.85).aspx">IX509AttributeArchiveKeyHash</a> object. The two methods complement each other. The <b>InitializeEncodeFromEncryptedKeyBlob</b> method enables you to construct an encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="https://msdn.microsoft.com/en-us/library/Aa377061(v=VS.85).aspx">EncryptedKeyHashBlob</a> property to retrieve the raw data.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377060(v=VS.85).aspx">IX509AttributeArchiveKeyHash</a>
 

 

