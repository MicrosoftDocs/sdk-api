---
UID: NF:certenroll.IX509Enrollment.CreateRequest
title: IX509Enrollment::CreateRequest
author: windows-sdk-content
description: Retrieves an encoded certificate request.
old-location: security\ix509enrollment_createrequest_method.htm
tech.root: SecCertEnroll
ms.assetid: bc01a648-04c7-411e-8f7a-80f19433a200
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateRequest, CreateRequest method [Security], CreateRequest method [Security],IX509Enrollment interface, IX509Enrollment interface [Security],CreateRequest method, IX509Enrollment.CreateRequest, IX509Enrollment::CreateRequest, certenroll/IX509Enrollment::CreateRequest, security.ix509enrollment_createrequest_method
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
 - IX509Enrollment.CreateRequest
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
- IX509Enrollment.CreateRequest
: 
---

# IX509Enrollment::CreateRequest


## -description


The <b>CreateRequest</b> method retrieves an encoded certificate request. The certificate request is contained in a byte array that is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by a string that is  either a pure binary sequence or Unicode encoded. This method is web enabled.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the DER-encoded request. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


### -param pValue [out]

Pointer to a <b>BSTR</b> variable that contains the DER-encoded request.


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
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate request cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>OLE_E_BLANK</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The enrollment object has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>CreateRequest</b> method calls the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, if necessary, to encode the raw data from the associated request object.

This method uses the information provided during initialization and other properties that have been specified, creates a dummy certificate and places it in the request store. The method also creates a key pair if necessary. Depending on how you initialize the enrollment object and on what properties you set, there may be no need to create a key pair. For example, if you are renewing a certificate by using an existing key, or if the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object associated with the certificate request represents an existing key, this method does not create a new key pair.

If a smartcard is involved, this method encodes external properties as extensions, includes them in the dummy certificate, and writes the dummy certificate to the smartcard key container. Smartcard logon certificates are encoded to the request store, not the personal store.

Before calling the <b>CreateRequest</b> method, you must initialize the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/3bf4ce4a-6556-403c-8334-a6bf01f074a3">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/04cb00af-f786-4548-bee3-2cc5083278c3">InitializeFromRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/44a934f4-9ae9-4f52-9d44-f5fcf30f3837">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

