---
UID: NF:certenroll.IX509ExtensionEnhancedKeyUsage.InitializeEncode
title: IX509ExtensionEnhancedKeyUsage::InitializeEncode
author: windows-sdk-content
description: Initializes the extension from a collection of IObjectId object identifiers (OIDs) that specify the intended uses of the public key.
old-location: security\ix509extensionenhancedkeyusage_initializeencode_method.htm
old-project: seccertenroll
ms.assetid: 6cb12736-db5d-4d65-b32f-4bd11ceea01d
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509ExtensionEnhancedKeyUsage interface [Security],InitializeEncode method, IX509ExtensionEnhancedKeyUsage.InitializeEncode, IX509ExtensionEnhancedKeyUsage::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionEnhancedKeyUsage interface, certenroll/IX509ExtensionEnhancedKeyUsage::InitializeEncode, security.ix509extensionenhancedkeyusage_initializeencode_method
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
 - IX509ExtensionEnhancedKeyUsage.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionEnhancedKeyUsage::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a collection of <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a>  object identifiers (OIDs) that specify the intended uses of the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>. This method is web enabled.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> interface.


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



You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/e83d0577-8eb9-4a59-8f52-ce1d9ab7f58a">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/0b9606d0-351c-4d2d-b876-545a9c2cf916">IX509ExtensionEnhancedKeyUsage</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the extension <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/17a92139-0f6c-4371-b6cb-44185752abce">EnhancedKeyUsage</a> property retrieves the collection of OIDs that identify the intended uses of the public key (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/0b9606d0-351c-4d2d-b876-545a9c2cf916">IX509ExtensionEnhancedKeyUsage</a>
 

 

