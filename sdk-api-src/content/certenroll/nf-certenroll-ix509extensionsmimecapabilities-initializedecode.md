---
UID: NF:certenroll.IX509ExtensionSmimeCapabilities.InitializeDecode
title: IX509ExtensionSmimeCapabilities::InitializeDecode
author: windows-sdk-content
description: Initializes the extension from a Distinguished Encoding Rules (DER) encoded byte array that contains the extension value.
old-location: security\ix509extensionsmimecapabilities_initializedecode_method.htm
tech.root: seccertenroll
ms.assetid: 9b89b9aa-3e71-4511-8e5a-1fe2165fa672
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509ExtensionSmimeCapabilities interface [Security],InitializeDecode method, IX509ExtensionSmimeCapabilities.InitializeDecode, IX509ExtensionSmimeCapabilities::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509ExtensionSmimeCapabilities interface, certenroll/IX509ExtensionSmimeCapabilities::InitializeDecode, security.ix509extensionsmimecapabilities_initializedecode_method
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
 - IX509ExtensionSmimeCapabilities.InitializeDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionSmimeCapabilities::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the  extension from a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value. The DER-encoded byte array is represented by a Unicode encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the <i>strEncodedData</i> parameter.


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



 You can use this method if you have a DER-encoded ASN.1 object that contains a <b>SmimeCapabilities</b> extension. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/731e3c93-699b-4a99-8520-294f3134aa66">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an  <a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the extension OID.</li>
<li>The <a href="https://msdn.microsoft.com/6e3ce718-16f9-47df-aff9-38e922fe505c">SmimeCapabilities</a> property retrieves the collection of capabilities (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a>
 

 

