---
UID: NF:xpsdigitalsignature.IXpsSignature.GetSignatureXml
title: IXpsSignature::GetSignatureXml (xpsdigitalsignature.h)
description: Gets the XML markup of the digital signature.
helpviewer_keywords: ["GetSignatureXml","GetSignatureXml method [XPS Documents and Packaging]","GetSignatureXml method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetSignatureXml method","IXpsSignature.GetSignatureXml","IXpsSignature::GetSignatureXml","xps.ixpssignature_getsignaturexml","xpsdigitalsignature/IXpsSignature::GetSignatureXml"]
old-location: xps\ixpssignature_getsignaturexml.htm
tech.root: xps
ms.assetid: 9e76487c-465c-4d15-82d0-ed2a21decc33
ms.date: 12/05/2018
ms.keywords: GetSignatureXml, GetSignatureXml method [XPS Documents and Packaging], GetSignatureXml method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetSignatureXml method, IXpsSignature.GetSignatureXml, IXpsSignature::GetSignatureXml, xps.ixpssignature_getsignaturexml, xpsdigitalsignature/IXpsSignature::GetSignatureXml
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
 - IXpsSignature::GetSignatureXml
 - xpsdigitalsignature/IXpsSignature::GetSignatureXml
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
 - IXpsSignature.GetSignatureXml
---

# IXpsSignature::GetSignatureXml


## -description

Gets the XML markup of the digital signature.

## -parameters

### -param signatureXml [out]

The XML markup of the digital signature.

### -param count [out]

The size, in bytes, of the buffer referenced by <i>signatureXml</i>.

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

This method allocates the memory buffer whose pointer is returned in <i>signatureXml</i>.  If <i>signatureXml</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>