---
UID: NF:certenroll.IX509CertificateRequestCmc2.CheckCertificateSignature
title: IX509CertificateRequestCmc2::CheckCertificateSignature method
author: windows-driver-content
description: Verifies the signature for a specified signer.
old-location: security\ix509certificaterequestcmc2_checkcertificatesignature.htm
old-project: SecCertEnroll
ms.assetid: 10ccda23-98d7-49ad-bb0c-60050d01892d
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: CheckCertificateSignature method [Security], CheckCertificateSignature method [Security], IX509CertificateRequestCmc2 interface, CheckCertificateSignature,IX509CertificateRequestCmc2.CheckCertificateSignature, IX509CertificateRequestCmc2, IX509CertificateRequestCmc2 interface [Security], CheckCertificateSignature method, IX509CertificateRequestCmc2::CheckCertificateSignature, certenroll/IX509CertificateRequestCmc2::CheckCertificateSignature, security.ix509certificaterequestcmc2_checkcertificatesignature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenroll.h
api_name:
-	IX509CertificateRequestCmc2.CheckCertificateSignature
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509CertificateRequestCmc2::CheckCertificateSignature method


## -description


The <b>CheckCertificateSignature</b> method verifies the signature for a specified signer.


## -parameters




### -param pSignerCertificate [in]

Pointer to an <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> interface that represents a signing certificate.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSignerCertificate</i> parameter cannot be <b>NULL</b>.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/27edf846-472e-4a22-bd3c-88044a1fbd99">IX509CertificateRequestCmc2</a>
 

 

