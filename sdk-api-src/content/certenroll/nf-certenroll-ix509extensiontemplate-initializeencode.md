---
UID: NF:certenroll.IX509ExtensionTemplate.InitializeEncode
title: IX509ExtensionTemplate::InitializeEncode
author: windows-sdk-content
description: Initializes the extension from a template object identifier (OID) and from major and minor version numbers.
old-location: security\ix509extensiontemplate_initializeencode_method.htm
tech.root: SecCertEnroll
ms.assetid: 93590649-78b4-4f78-81b8-5c21cf91608d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509ExtensionTemplate interface [Security],InitializeEncode method, IX509ExtensionTemplate.InitializeEncode, IX509ExtensionTemplate::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::InitializeEncode, security.ix509extensiontemplate_initializeencode_method
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
 - IX509ExtensionTemplate.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509ExtensionTemplate.InitializeEncode
: 
---

# IX509ExtensionTemplate::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from a template <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) and from major and minor version numbers. This method is web enabled.


## -parameters




### -param pTemplateOid [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface that represents the template OID.


### -param MajorVersion [in]

A <b>LONG</b> variable that contains the major version number of the template. The default value is zero (0).


### -param MinorVersion [in]

A <b>LONG</b> variable that contains the minor version number of the template. The default value is zero (0).


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



You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa378307(v=VS.85).aspx">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378314(v=VS.85).aspx">MajorVersion</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa378343(v=VS.85).aspx">MinorVersion</a> properties retrieve the version information.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378403(v=VS.85).aspx">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>


You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa378307(v=VS.85).aspx">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378108(v=VS.85).aspx">IX509ExtensionBasicConstraints</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded ASN.1 structure. You can retrieve the raw data for the extension by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa378314(v=VS.85).aspx">MajorVersion</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa378343(v=VS.85).aspx">MinorVersion</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa378403(v=VS.85).aspx">TemplateOid</a> properties.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
 

 

