---
UID: NF:certenroll.IX509ExtensionBasicConstraints.InitializeEncode
title: IX509ExtensionBasicConstraints::InitializeEncode
author: windows-sdk-content
description: Initializes the extension from a Boolean value that indicates whether the certificate subject is a certification authority (CA) and an integer that contains the depth of the subordinate CA chain.
old-location: security\ix509extensionbasicconstraints_initializeencode_method.htm
old-project: SecCertEnroll
ms.assetid: e9a08445-8fc5-45cc-a2c6-ec62470e5c55
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509ExtensionBasicConstraints interface [Security],InitializeEncode method, IX509ExtensionBasicConstraints.InitializeEncode, IX509ExtensionBasicConstraints::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionBasicConstraints interface, certenroll/IX509ExtensionBasicConstraints::InitializeEncode, security.ix509extensionbasicconstraints_initializeencode_method
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
 - IX509ExtensionBasicConstraints.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionBasicConstraints::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a Boolean value that indicates whether the certificate subject is a certification authority (CA) and an integer that contains the depth of the subordinate CA chain.


## -parameters




### -param IsCA [in]

A <b>VARIANT_BOOL</b> variable that specifies whether the certificate subject is a CA.


### -param PathLenConstraint [in]

A <b>LONG</b> variable that contains the maximum number of certificates in the chain.


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



 The method associates the name collection with the XCN_OID_BASIC_CONSTRAINTS2 (2.5.29.19) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and encodes it by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/3b0b5547-6871-412a-8463-889af3b1302b">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/81a1d567-191f-463c-ba67-0867025d8756">IX509ExtensionBasicConstraints</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://msdn.microsoft.com/1547d015-b497-4f91-acc2-4cbb2a69709f">IsCA</a> property identifies whether the certificate subject can be a certification authority.</li>
<li>The <a href="https://msdn.microsoft.com/6d688596-60fd-47d0-8f91-cfda448ac015">PathLenConstraint</a> property identifies the depth of the subordinate certification authority chain.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/81a1d567-191f-463c-ba67-0867025d8756">IX509ExtensionBasicConstraints</a>
 

 

