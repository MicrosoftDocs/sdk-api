---
UID: NF:xpsdigitalsignature.IXpsSignature.SetSignatureXml
title: IXpsSignature::SetSignatureXml (xpsdigitalsignature.h)
description: Sets the XML markup of the digital signature.
helpviewer_keywords: ["IXpsSignature interface [XPS Documents and Packaging]","SetSignatureXml method","IXpsSignature.SetSignatureXml","IXpsSignature::SetSignatureXml","SetSignatureXml","SetSignatureXml method [XPS Documents and Packaging]","SetSignatureXml method [XPS Documents and Packaging]","IXpsSignature interface","xps.ixpssignature_setsignaturexml","xpsdigitalsignature/IXpsSignature::SetSignatureXml"]
old-location: xps\ixpssignature_setsignaturexml.htm
tech.root: xps
ms.assetid: 3ba32f16-2e11-479c-bc3c-0982e90b883d
ms.date: 12/05/2018
ms.keywords: IXpsSignature interface [XPS Documents and Packaging],SetSignatureXml method, IXpsSignature.SetSignatureXml, IXpsSignature::SetSignatureXml, SetSignatureXml, SetSignatureXml method [XPS Documents and Packaging], SetSignatureXml method [XPS Documents and Packaging],IXpsSignature interface, xps.ixpssignature_setsignaturexml, xpsdigitalsignature/IXpsSignature::SetSignatureXml
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
 - IXpsSignature::SetSignatureXml
 - xpsdigitalsignature/IXpsSignature::SetSignatureXml
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
 - IXpsSignature.SetSignatureXml
---

# IXpsSignature::SetSignatureXml


## -description

Sets the XML markup of the digital signature.

## -parameters

### -param signatureXml [in]

The XML markup of the digital signature.

### -param count [in]

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>signatureXml</i> is <b>NULL</b>.

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

Before calling this method, the application must check that the signature markup is valid. If the signature markup is not valid, this method will fail and the content of the signature part will not be changed.

<div class="alert"><b>Warning</b>  <p class="note">Using this method to create digital signatures might cause other methods of this interface to return signatures and data that are no longer valid.

</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>