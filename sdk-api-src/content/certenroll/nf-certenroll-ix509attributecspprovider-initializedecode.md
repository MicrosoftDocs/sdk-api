---
UID: NF:certenroll.IX509AttributeCspProvider.InitializeDecode
title: IX509AttributeCspProvider::InitializeDecode
author: windows-sdk-content
description: Initializes the object from a Distinguished Encoding Rules (DER) encoded byte array that contains information about the provider.
old-location: security\ix509attributecspprovider_initializedecode_method.htm
old-project: SecCertEnroll
ms.assetid: 7098ee8d-39e9-4463-97fe-309265c6baa7
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509AttributeCspProvider interface [Security],InitializeDecode method, IX509AttributeCspProvider.InitializeDecode, IX509AttributeCspProvider::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::InitializeDecode, security.ix509attributecspprovider_initializedecode_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509AttributeCspProvider.InitializeDecode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeCspProvider::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains information about the provider. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded attribute.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENROLLMENT_CSP_PROVIDER</b> (1.3.6.1.4.1.311.13.2.2). For more information, see <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a>.

You can use this method if you have a DER-encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) object that contains the attribute value. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/b0b45ea2-b682-4065-8624-08c34581b5ea">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an <a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://msdn.microsoft.com/4bb04097-9e6c-4b15-852e-be86d21637bf">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06245293-b331-4963-a0cf-b7c604580908">Signature</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>
 

 

