---
UID: NF:certenroll.IX509ExtensionSubjectKeyIdentifier.InitializeEncode
title: IX509ExtensionSubjectKeyIdentifier::InitializeEncode
author: windows-sdk-content
description: Initializes the extension from a byte array that contains the key identifier.
old-location: security\ix509extensionsubjectkeyidentifier_initializeencode_method.htm
tech.root: SecCertEnroll
ms.assetid: 0faf3567-3908-473e-9f5c-392991ea668c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509ExtensionSubjectKeyIdentifier interface [Security],InitializeEncode method, IX509ExtensionSubjectKeyIdentifier.InitializeEncode, IX509ExtensionSubjectKeyIdentifier::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionSubjectKeyIdentifier interface, certenroll/IX509ExtensionSubjectKeyIdentifier::InitializeEncode, security.ix509extensionsubjectkeyidentifier_initializeencode_method
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
 - IX509ExtensionSubjectKeyIdentifier.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionSubjectKeyIdentifier::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a byte array that contains the key identifier. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the <i>strKeyIdentifier</i> parameter.


### -param strKeyIdentifier [in]

A <b>BSTR</b> variable that contains the key identifier.


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



Typically, the input value should be a SHA-1 hash of the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> contained in the certification authority signing certificate. The method associates the value with the XCN_OID_SUBJECT_KEY_IDENTIFIER (2.5.29.14) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and encodes it by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/5886187d-33b1-4151-a01f-de263c41c27b">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://msdn.microsoft.com/6ebb3f2f-c7ec-4898-a47b-681d510a7c6d">AuthorityKeyIdentifier</a> property retrieves the raw data.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a>
 

 

