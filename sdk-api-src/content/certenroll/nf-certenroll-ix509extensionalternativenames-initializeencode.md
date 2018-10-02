---
UID: NF:certenroll.IX509ExtensionAlternativeNames.InitializeEncode
title: IX509ExtensionAlternativeNames::InitializeEncode
author: windows-sdk-content
description: Initializes the extension from an IAlternativeNames collection.
old-location: security\ix509extensionalternativenames_initializeencode_method.htm
tech.root: SecCertEnroll
ms.assetid: e520b2b4-c181-4fb1-98e8-f159bd0d31b4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509ExtensionAlternativeNames interface [Security],InitializeEncode method, IX509ExtensionAlternativeNames.InitializeEncode, IX509ExtensionAlternativeNames::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionAlternativeNames interface, certenroll/IX509ExtensionAlternativeNames::InitializeEncode, security.ix509extensionalternativenames_initializeencode_method
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
 - IX509ExtensionAlternativeNames.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionAlternativeNames::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension from an <a href="https://msdn.microsoft.com/en-us/library/Aa374984(v=VS.85).aspx">IAlternativeNames</a> collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa374984(v=VS.85).aspx">IAlternativeNames</a> interface.


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



 The method associates the name collection with the XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17) <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) and encodes it by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa378087(v=VS.85).aspx">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378081(v=VS.85).aspx">IX509ExtensionAlternativeNames</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a DER-encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

 You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378085(v=VS.85).aspx">AlternativeNames</a> property retrieves the collection of names (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378081(v=VS.85).aspx">IX509ExtensionAlternativeNames</a>
 

 

