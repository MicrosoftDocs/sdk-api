---
UID: NF:certenroll.IX509ExtensionTemplate.InitializeDecode
title: IX509ExtensionTemplate::InitializeDecode
author: windows-sdk-content
description: Initializes the extension from a DER-encoded byte array that contains the extension value.
old-location: security\ix509extensiontemplate_initializedecode_method.htm
old-project: seccertenroll
ms.assetid: c35a6108-9f5e-4876-9ea1-ce8b568abfde
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509ExtensionTemplate interface [Security],InitializeDecode method, IX509ExtensionTemplate.InitializeDecode, IX509ExtensionTemplate::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::InitializeDecode, security.ix509extensiontemplate_initializedecode_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - IX509ExtensionTemplate.InitializeDecode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionTemplate::InitializeDecode


## -description


The <b>InitializeDecode</b> method initializes the  extension from a DER-encoded byte array that contains the extension value. The encoded byte array is represented by a Unicode encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the <i>strEncodedData</i> parameter.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded extension.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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



You can use this method if you have a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) object that contains a <b>CertificateTemplate</b> extension.  You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa375047(v=VS.85).aspx">IBinaryConverter</a> interface.

You must call either <a href="https://msdn.microsoft.com/en-us/library/Aa378310(v=VS.85).aspx">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded ASN.1 extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378314(v=VS.85).aspx">MajorVersion</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa378343(v=VS.85).aspx">MinorVersion</a> properties retrieve the version information.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378403(v=VS.85).aspx">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
 

 

