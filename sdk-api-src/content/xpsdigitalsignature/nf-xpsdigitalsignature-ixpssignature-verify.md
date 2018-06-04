---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IXpsSignature::Verify


## -description


Verifies the signature against a specified X.509 certificate.


## -parameters




### -param x509Certificate [in]

The <a href="_crypto2_cert_context">CERT_CONTEXT</a> structure that contains the X.509 certificate that will be used for verification.

If the signature is not incomplete or incompliant, this  certificate will be used  only to  validate that the signed data in the XPS package is intact. The certificate will not be used to perform any other checks.
    Before using the certificate the application is expected to verify the trust chain and any other requirements.


### -param sigStatus [out, retval]

The <a href="https://msdn.microsoft.com/8c03749c-49cf-4d9c-90be-a75412f044ec">XPS_SIGNATURE_STATUS</a> value that describes the results of the verification.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a> and  <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>x509Certificate</i> or  <i>sigStatus</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not connected to the signature manager.

</td>
</tr>
</table>
 




## -remarks



This method detects the signature status in the order that is specified in section 10.2.1.2 of the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.
    The sequence of detection is as follows: incompliant, incomplete, broken, questionable, and, finally, valid.
    This means that  if, for example,  a signature is found to be incompliant, no digest will be calculated  if the signature is also broken.

For more information on the different types of signature statuses that can be detected by this method, see  <a href="https://msdn.microsoft.com/8c03749c-49cf-4d9c-90be-a75412f044ec">XPS_SIGNATURE_STATUS</a>.




## -see-also




<a href="_crypto2_cert_context">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/8c03749c-49cf-4d9c-90be-a75412f044ec">XPS_SIGNATURE_STATUS</a>
 

 

