---
UID: NF:certenroll.IX509ExtensionTemplateName.InitializeEncode
title: IX509ExtensionTemplateName::InitializeEncode
author: windows-sdk-content
description: Initializes the extension from a string that contains the template name.
old-location: security\ix509extensiontemplatename_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: 8b72b73a-bfd5-4a56-a106-01f2fd59e922
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509ExtensionTemplateName interface [Security],InitializeEncode method, IX509ExtensionTemplateName.InitializeEncode, IX509ExtensionTemplateName::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionTemplateName interface, certenroll/IX509ExtensionTemplateName::InitializeEncode, security.ix509extensiontemplatename_initializeencode_method
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
 - IX509ExtensionTemplateName.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplateName::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a string that contains the template name.  This method is web enabled.


## -parameters




### -param strTemplateName [in]

A <b>BSTR</b> variable that contains the name.


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



You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/05fb275c-75b2-4619-8d6a-c6c9868d9765">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/b403a27f-e477-4445-adcb-5fce58453727">TemplateName</a> property retrieves the template name (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a>
 

 

