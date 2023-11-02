---
UID: NF:xpsdigitalsignature.IXpsSignature.Verify
title: IXpsSignature::Verify (xpsdigitalsignature.h)
description: Verifies the signature against a specified X.509 certificate.
helpviewer_keywords: ["IXpsSignature interface [XPS Documents and Packaging]","Verify method","IXpsSignature.Verify","IXpsSignature::Verify","Verify","Verify method [XPS Documents and Packaging]","Verify method [XPS Documents and Packaging]","IXpsSignature interface","xps.ixpssignature_verify","xpsdigitalsignature/IXpsSignature::Verify"]
old-location: xps\ixpssignature_verify.htm
tech.root: xps
ms.assetid: 6f3239dd-e29f-4340-a4ad-49ceb6a151de
ms.date: 12/05/2018
ms.keywords: IXpsSignature interface [XPS Documents and Packaging],Verify method, IXpsSignature.Verify, IXpsSignature::Verify, Verify, Verify method [XPS Documents and Packaging], Verify method [XPS Documents and Packaging],IXpsSignature interface, xps.ixpssignature_verify, xpsdigitalsignature/IXpsSignature::Verify
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsSignature::Verify
 - xpsdigitalsignature/IXpsSignature::Verify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignature.Verify
---

# IXpsSignature::Verify


## -description

Verifies the signature against a specified X.509 certificate.

## -parameters

### -param x509Certificate [in]

The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the X.509 certificate that will be used for verification.

If the signature is not incomplete or incompliant, this  certificate will be used  only to  validate that the signed data in the XPS package is intact. The certificate will not be used to perform any other checks.
    Before using the certificate the application is expected to verify the trust chain and any other requirements.

### -param sigStatus [out, retval]

The <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status">XPS_SIGNATURE_STATUS</a> value that describes the results of the verification.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a> and  <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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

This method detects the signature status in the order that is specified in section 10.2.1.2 of the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.
    The sequence of detection is as follows: incompliant, incomplete, broken, questionable, and, finally, valid.
    This means that  if, for example,  a signature is found to be incompliant, no digest will be calculated  if the signature is also broken.

For more information on the different types of signature statuses that can be detected by this method, see  <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status">XPS_SIGNATURE_STATUS</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status">XPS_SIGNATURE_STATUS</a>