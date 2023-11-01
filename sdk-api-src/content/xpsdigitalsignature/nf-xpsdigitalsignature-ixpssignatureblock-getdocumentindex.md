---
UID: NF:xpsdigitalsignature.IXpsSignatureBlock.GetDocumentIndex
title: IXpsSignatureBlock::GetDocumentIndex (xpsdigitalsignature.h)
description: Gets the index of the FixedDocument part that references the SignatureDefinitions part that corresponds to this signature block.
helpviewer_keywords: ["GetDocumentIndex","GetDocumentIndex method [XPS Documents and Packaging]","GetDocumentIndex method [XPS Documents and Packaging]","IXpsSignatureBlock interface","IXpsSignatureBlock interface [XPS Documents and Packaging]","GetDocumentIndex method","IXpsSignatureBlock.GetDocumentIndex","IXpsSignatureBlock::GetDocumentIndex","xps.ixpssignatureblock_getdocumentindex","xpsdigitalsignature/IXpsSignatureBlock::GetDocumentIndex"]
old-location: xps\ixpssignatureblock_getdocumentindex.htm
tech.root: printdocs
ms.assetid: 5e9052d9-9a27-41fe-8842-50033cb8edf2
ms.date: 12/05/2018
ms.keywords: GetDocumentIndex, GetDocumentIndex method [XPS Documents and Packaging], GetDocumentIndex method [XPS Documents and Packaging],IXpsSignatureBlock interface, IXpsSignatureBlock interface [XPS Documents and Packaging],GetDocumentIndex method, IXpsSignatureBlock.GetDocumentIndex, IXpsSignatureBlock::GetDocumentIndex, xps.ixpssignatureblock_getdocumentindex, xpsdigitalsignature/IXpsSignatureBlock::GetDocumentIndex
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
 - IXpsSignatureBlock::GetDocumentIndex
 - xpsdigitalsignature/IXpsSignatureBlock::GetDocumentIndex
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
 - IXpsSignatureBlock.GetDocumentIndex
---

# IXpsSignatureBlock::GetDocumentIndex


## -description

Gets the index of the FixedDocument part that references the SignatureDefinitions part that corresponds to this signature block.

## -parameters

### -param fixedDocumentIndex [out, retval]

The zero-based index of the FixedDocument part that references the SignatureDefinitions part that corresponds to this SignatureBlock.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>fixedDocumentIndex</i> is <b>NULL</b>.

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

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>