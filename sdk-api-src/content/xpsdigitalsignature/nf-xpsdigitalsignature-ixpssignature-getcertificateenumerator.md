---
UID: NF:xpsdigitalsignature.IXpsSignature.GetCertificateEnumerator
title: IXpsSignature::GetCertificateEnumerator (xpsdigitalsignature.h)
description: Gets a pointer to an IOpcCertificateEnumerator interface, which enumerates the package certificates that are attached to the signature.
helpviewer_keywords: ["GetCertificateEnumerator","GetCertificateEnumerator method [XPS Documents and Packaging]","GetCertificateEnumerator method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetCertificateEnumerator method","IXpsSignature.GetCertificateEnumerator","IXpsSignature::GetCertificateEnumerator","xps.ixpssignature_getcertificateenumerator","xpsdigitalsignature/IXpsSignature::GetCertificateEnumerator"]
old-location: xps\ixpssignature_getcertificateenumerator.htm
tech.root: xps
ms.assetid: e4af0aa3-8420-4297-993c-dda4d4f7cf61
ms.date: 12/05/2018
ms.keywords: GetCertificateEnumerator, GetCertificateEnumerator method [XPS Documents and Packaging], GetCertificateEnumerator method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetCertificateEnumerator method, IXpsSignature.GetCertificateEnumerator, IXpsSignature::GetCertificateEnumerator, xps.ixpssignature_getcertificateenumerator, xpsdigitalsignature/IXpsSignature::GetCertificateEnumerator
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
 - IXpsSignature::GetCertificateEnumerator
 - xpsdigitalsignature/IXpsSignature::GetCertificateEnumerator
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
 - IXpsSignature.GetCertificateEnumerator
---

# IXpsSignature::GetCertificateEnumerator


## -description

Gets a pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a> interface, which enumerates the package certificates that are attached to the signature.

## -parameters

### -param certificateEnumerator [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a> interface, which enumerates the certificates that are attached to the signature.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not connected to the signature manager.

</td>
</tr>
</table>

## -remarks

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a> interface returned in <i>certificateEnumerator</i> can be empty; however the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a> requires that at least the signing certificate be included in the XPS package. Package producers may include additional certificates as well. For example, the entire certificate trust chain could be included in the XPS package.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>