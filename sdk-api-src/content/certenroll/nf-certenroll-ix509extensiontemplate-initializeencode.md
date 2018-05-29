---
UID: NF:certenroll.IX509ExtensionTemplate.InitializeEncode
title: IX509ExtensionTemplate::InitializeEncode
author: windows-sdk-content
description: Initializes the extension from a template object identifier (OID) and from major and minor version numbers.
old-location: security\ix509extensiontemplate_initializeencode_method.htm
old-project: SecCertEnroll
ms.assetid: 93590649-78b4-4f78-81b8-5c21cf91608d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509ExtensionTemplate interface [Security],InitializeEncode method, IX509ExtensionTemplate.InitializeEncode, IX509ExtensionTemplate::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::InitializeEncode, security.ix509extensiontemplate_initializeencode_method
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
-	IX509ExtensionTemplate.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionTemplate::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a template <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and from major and minor version numbers. This method is web enabled.


## -parameters




### -param pTemplateOid [in]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that represents the template OID.


### -param MajorVersion [in]

A <b>LONG</b> variable that contains the major version number of the template. The default value is zero (0).


### -param MinorVersion [in]

A <b>LONG</b> variable that contains the minor version number of the template. The default value is zero (0).


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



You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/c35a6108-9f5e-4876-9ea1-ce8b568abfde">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://msdn.microsoft.com/35057dbc-4518-4f76-bf82-9d9a8abe5525">MajorVersion</a> and <a href="https://msdn.microsoft.com/0fb17099-4bf6-405c-8b54-4280a8023256">MinorVersion</a> properties retrieve the version information.</li>
<li>The <a href="https://msdn.microsoft.com/9106f995-4d74-464a-8ca3-aec056199ace">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>


You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/c35a6108-9f5e-4876-9ea1-ce8b568abfde">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/81a1d567-191f-463c-ba67-0867025d8756">IX509ExtensionBasicConstraints</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded ASN.1 structure. You can retrieve the raw data for the extension by calling the <a href="https://msdn.microsoft.com/35057dbc-4518-4f76-bf82-9d9a8abe5525">MajorVersion</a>, <a href="https://msdn.microsoft.com/0fb17099-4bf6-405c-8b54-4280a8023256">MinorVersion</a>, and <a href="https://msdn.microsoft.com/9106f995-4d74-464a-8ca3-aec056199ace">TemplateOid</a> properties.




## -see-also




<a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a>
 

 

