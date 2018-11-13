---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.InitializeDecode
title: IX509AttributeArchiveKeyHash::InitializeDecode
author: windows-sdk-content
description: Initializes the object from a Distinguished Encoding Rules (DER) encoded byte array that contains a SHA-1 hash of the encrypted private key.
old-location: security\ix509attributearchivekeyhash_initializedecode_method.htm
tech.root: SecCertEnroll
ms.assetid: c8f59fba-c6ce-4e11-bb25-8a6fd23218d1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509AttributeArchiveKeyHash interface [Security],InitializeDecode method, IX509AttributeArchiveKeyHash.InitializeDecode, IX509AttributeArchiveKeyHash::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509AttributeArchiveKeyHash interface, certenroll/IX509AttributeArchiveKeyHash::InitializeDecode, security.ix509attributearchivekeyhash_initializedecode_method
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
 - IX509AttributeArchiveKeyHash.InitializeDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeArchiveKeyHash::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains a SHA-1 <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hash</a> of  the encrypted <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains hash value.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded attribute.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENCRYPTED_KEY_HASH</b> (1.3.6.1.4.1.311.21.21). For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a>.

You can use this method if you have a DER-encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) object that contains the attribute value. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa375047(v=VS.85).aspx">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/en-us/library/Aa377063(v=VS.85).aspx">InitializeEncodeFromEncryptedKeyBlob</a> or <b>InitializeDecode</b> before you can use an <a href="https://msdn.microsoft.com/en-us/library/Aa377060(v=VS.85).aspx">IX509AttributeArchiveKeyHash</a> object. The two methods complement each other. The <b>InitializeEncodeFromEncryptedKeyBlob</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="https://msdn.microsoft.com/en-us/library/Aa377061(v=VS.85).aspx">EncryptedKeyHashBlob</a> property to retrieve the raw data.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377060(v=VS.85).aspx">IX509AttributeArchiveKeyHash</a>
 

 

