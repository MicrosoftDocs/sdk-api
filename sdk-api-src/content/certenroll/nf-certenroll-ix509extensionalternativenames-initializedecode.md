---
UID: NF:certenroll.IX509ExtensionAlternativeNames.InitializeDecode
title: IX509ExtensionAlternativeNames::InitializeDecode
author: windows-driver-content
description: Initializes the extension from a Distinguished Encoding Rules (DER) encoded byte array that contains the extension value.
old-location: security\ix509extensionalternativenames_initializedecode_method.htm
old-project: SecCertEnroll
ms.assetid: a314dfac-fe17-4e33-b528-491a2622e80c
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509ExtensionAlternativeNames interface [Security],InitializeDecode method, IX509ExtensionAlternativeNames.InitializeDecode, IX509ExtensionAlternativeNames::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509ExtensionAlternativeNames interface, certenroll/IX509ExtensionAlternativeNames::InitializeDecode, security.ix509extensionalternativenames_initializedecode_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509ExtensionAlternativeNames.InitializeDecode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionAlternativeNames::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the  extension from a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value. The encoded byte array is represented by a Unicode encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the <i>strEncodedData</i> value.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded extension.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



 You can use this method if you have a DER-encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) object that contains an <b>AlternativeNames</b> extension. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/e520b2b4-c181-4fb1-98e8-f159bd0d31b4">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an  <a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/816afa9d-2283-4e17-ad12-ee53e5353d83">AlternativeNames</a> property retrieves the collection of names (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
 

 

