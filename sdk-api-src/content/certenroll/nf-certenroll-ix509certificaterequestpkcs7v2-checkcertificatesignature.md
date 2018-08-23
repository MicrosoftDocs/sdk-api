---
UID: NF:certenroll.IX509CertificateRequestPkcs7V2.CheckCertificateSignature
title: IX509CertificateRequestPkcs7V2::CheckCertificateSignature
author: windows-sdk-content
description: Verifies the certificate signature.
old-location: security\ix509certificaterequestpkcs7v2_checkcertificatesignature.htm
old-project: seccertenroll
ms.assetid: 6ee30e16-1901-45dc-8023-ef605d8a4d21
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CheckCertificateSignature, CheckCertificateSignature method [Security], CheckCertificateSignature method [Security],IX509CertificateRequestPkcs7V2 interface, IX509CertificateRequestPkcs7V2 interface [Security],CheckCertificateSignature method, IX509CertificateRequestPkcs7V2.CheckCertificateSignature, IX509CertificateRequestPkcs7V2::CheckCertificateSignature, certenroll/IX509CertificateRequestPkcs7V2::CheckCertificateSignature, security.ix509certificaterequestpkcs7v2_checkcertificatesignature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
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
 - Certenroll.h
api_name:
 - IX509CertificateRequestPkcs7V2.CheckCertificateSignature
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509CertificateRequestPkcs7V2::CheckCertificateSignature


## -description


The <b>CheckCertificateSignature</b> method verifies the certificate signature.


## -parameters




### -param ValidateCertificateChain [in]

A Boolean value that specifies whether to also verify the certificate chain. This parameter can be <b>NULL</b>.


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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
A signer certificate cannot be found.

</td>
</tr>
</table>
 




## -remarks



A PKCS #7 request has exactly one certificate-based signature.




## -see-also




<a href="https://msdn.microsoft.com/e58e1122-2ef0-4902-a9e9-23934cc544ec">IX509CertificateRequestPkcs7V2</a>
 

 

