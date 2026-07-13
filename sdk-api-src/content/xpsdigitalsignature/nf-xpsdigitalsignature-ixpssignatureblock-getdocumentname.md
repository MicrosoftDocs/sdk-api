---
UID: NF:xpsdigitalsignature.IXpsSignatureBlock.GetDocumentName
title: IXpsSignatureBlock::GetDocumentName (xpsdigitalsignature.h)
description: Gets a pointer to the IOpcPartUri interface that contains the URI of the document part.
helpviewer_keywords: ["GetDocumentName","GetDocumentName method [XPS Documents and Packaging]","GetDocumentName method [XPS Documents and Packaging]","IXpsSignatureBlock interface","IXpsSignatureBlock interface [XPS Documents and Packaging]","GetDocumentName method","IXpsSignatureBlock.GetDocumentName","IXpsSignatureBlock::GetDocumentName","xps.ixpssignatureblock_getdocumentname","xpsdigitalsignature/IXpsSignatureBlock::GetDocumentName"]
old-location: xps\ixpssignatureblock_getdocumentname.htm
tech.root: xps
ms.assetid: f93e94ff-c56f-4b3c-8af8-983253bd5657
ms.date: 12/05/2018
ms.keywords: GetDocumentName, GetDocumentName method [XPS Documents and Packaging], GetDocumentName method [XPS Documents and Packaging],IXpsSignatureBlock interface, IXpsSignatureBlock interface [XPS Documents and Packaging],GetDocumentName method, IXpsSignatureBlock.GetDocumentName, IXpsSignatureBlock::GetDocumentName, xps.ixpssignatureblock_getdocumentname, xpsdigitalsignature/IXpsSignatureBlock::GetDocumentName
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
 - IXpsSignatureBlock::GetDocumentName
 - xpsdigitalsignature/IXpsSignatureBlock::GetDocumentName
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
 - IXpsSignatureBlock.GetDocumentName
---

# IXpsSignatureBlock::GetDocumentName


## -description

Gets a pointer to the  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the URI of the document part.

## -parameters

### -param fixedDocumentName [out, retval]

A pointer to the  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the URI of the document part.

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
<i>fixedDocumentName</i> is <b>NULL</b>.

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

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>