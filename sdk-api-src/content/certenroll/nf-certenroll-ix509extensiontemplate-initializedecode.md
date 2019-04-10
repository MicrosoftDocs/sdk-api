---
UID: NF:certenroll.IX509ExtensionTemplate.InitializeDecode
title: IX509ExtensionTemplate::InitializeDecode (certenroll.h)
author: windows-sdk-content
description: Initializes the extension from a DER-encoded byte array that contains the extension value.
old-location: security\ix509extensiontemplate_initializedecode_method.htm
tech.root: seccertenroll
ms.assetid: c35a6108-9f5e-4876-9ea1-ce8b568abfde
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplate interface [Security],InitializeDecode method, IX509ExtensionTemplate.InitializeDecode, IX509ExtensionTemplate::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::InitializeDecode, security.ix509extensiontemplate_initializedecode_method
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
 - IX509ExtensionTemplate.InitializeDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplate::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the  extension from a DER-encoded byte array that contains the extension value. The encoded byte array is represented by a Unicode encoded string.


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



You can use this method if you have a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) object that contains a <b>CertificateTemplate</b> extension.  You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/93590649-78b4-4f78-81b8-5c21cf91608d">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an  <a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/35057dbc-4518-4f76-bf82-9d9a8abe5525">MajorVersion</a> and <a href="https://msdn.microsoft.com/0fb17099-4bf6-405c-8b54-4280a8023256">MinorVersion</a> properties retrieve the version information.</li>
<li>The <a href="https://msdn.microsoft.com/9106f995-4d74-464a-8ca3-aec056199ace">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a>
 

 

