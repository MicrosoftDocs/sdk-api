---
UID: NF:certenroll.IX509ExtensionSmimeCapabilities.InitializeEncode
title: IX509ExtensionSmimeCapabilities::InitializeEncode method
author: windows-driver-content
description: Initializes the extension from an ISmimeCapabilities collection.
old-location: security\ix509extensionsmimecapabilities_initializeencode_method.htm
old-project: SecCertEnroll
ms.assetid: 731e3c93-699b-4a99-8520-294f3134aa66
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IX509ExtensionSmimeCapabilities, IX509ExtensionSmimeCapabilities interface [Security], InitializeEncode method, IX509ExtensionSmimeCapabilities::InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security], IX509ExtensionSmimeCapabilities interface, InitializeEncode,IX509ExtensionSmimeCapabilities.InitializeEncode, certenroll/IX509ExtensionSmimeCapabilities::InitializeEncode, security.ix509extensionsmimecapabilities_initializeencode_method
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
-	IX509ExtensionSmimeCapabilities.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionSmimeCapabilities::InitializeEncode method


## -description


The <b>InitializeEncode</b> method initializes the extension from an <a href="https://msdn.microsoft.com/f9750b68-9d35-4594-96fc-2fbd54a87dcc">ISmimeCapabilities</a> collection.


## -parameters




### -param pValue [in]

Pointer to the <a href="https://msdn.microsoft.com/f9750b68-9d35-4594-96fc-2fbd54a87dcc">ISmimeCapabilities</a> interface.


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



You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/9b89b9aa-3e71-4511-8e5a-1fe2165fa672">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the extension OID.</li>
<li>The <a href="https://msdn.microsoft.com/6e3ce718-16f9-47df-aff9-38e922fe505c">SmimeCapabilities</a> property retrieves the collection of capabilities (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/f9750b68-9d35-4594-96fc-2fbd54a87dcc">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a>
 

 

