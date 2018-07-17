---
UID: NF:certenroll.IX509ExtensionAuthorityKeyIdentifier.InitializeDecode
title: IX509ExtensionAuthorityKeyIdentifier::InitializeDecode
author: windows-sdk-content
description: Initializes the extension from a Distinguished Encoding Rules (DER) encoded byte array that contains the extension value.
old-location: security\ix509extensionauthoritykeyidentifier_initializedecode_method.htm
old-project: seccertenroll
ms.assetid: ce37bcba-05b1-4d42-8853-14fecbcb436b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IX509ExtensionAuthorityKeyIdentifier interface [Security],InitializeDecode method, IX509ExtensionAuthorityKeyIdentifier.InitializeDecode, IX509ExtensionAuthorityKeyIdentifier::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509ExtensionAuthorityKeyIdentifier interface, certenroll/IX509ExtensionAuthorityKeyIdentifier::InitializeDecode, security.ix509extensionauthoritykeyidentifier_initializedecode_method
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
 - IX509ExtensionAuthorityKeyIdentifier.InitializeDecode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionAuthorityKeyIdentifier::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the extension from a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value. The encoded byte array is represented by a Unicode encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string.


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



You can use this method if you have a DER-encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) object that contains an <b>AuthorityKeyIdentifier</b> extension.  You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/450e65f9-cca0-42bd-b70b-baaf2e353812">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an  <a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/6ebb3f2f-c7ec-4898-a47b-681d510a7c6d">AuthorityKeyIdentifier</a> property retrieves the raw data.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a>
 

 

