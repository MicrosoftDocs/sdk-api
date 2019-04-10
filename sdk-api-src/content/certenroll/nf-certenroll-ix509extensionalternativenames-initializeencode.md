---
UID: NF:certenroll.IX509ExtensionAlternativeNames.InitializeEncode
title: IX509ExtensionAlternativeNames::InitializeEncode (certenroll.h)
author: windows-sdk-content
description: Initializes the extension from an IAlternativeNames collection.
old-location: security\ix509extensionalternativenames_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: e520b2b4-c181-4fb1-98e8-f159bd0d31b4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509ExtensionAlternativeNames interface [Security],InitializeEncode method, IX509ExtensionAlternativeNames.InitializeEncode, IX509ExtensionAlternativeNames::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionAlternativeNames interface, certenroll/IX509ExtensionAlternativeNames::InitializeEncode, security.ix509extensionalternativenames_initializeencode_method
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
 - IX509ExtensionAlternativeNames.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionAlternativeNames::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from an <a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a> collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a> interface.


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



 The method associates the name collection with the XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and encodes it by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/a314dfac-fe17-4e33-b528-491a2622e80c">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

 You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://msdn.microsoft.com/816afa9d-2283-4e17-ad12-ee53e5353d83">AlternativeNames</a> property retrieves the collection of names (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
 

 

