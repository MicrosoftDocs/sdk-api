---
UID: NF:xpsdigitalsignature.IXpsSignatureBlock.GetPartName
title: IXpsSignatureBlock::GetPartName (xpsdigitalsignature.h)
description: Gets a pointer to the IOpcPartUri interface that contains the URI of the SignatureDefinitions part.
helpviewer_keywords: ["GetPartName","GetPartName method [XPS Documents and Packaging]","GetPartName method [XPS Documents and Packaging]","IXpsSignatureBlock interface","IXpsSignatureBlock interface [XPS Documents and Packaging]","GetPartName method","IXpsSignatureBlock.GetPartName","IXpsSignatureBlock::GetPartName","xps.ixpssignatureblock_getpartname","xpsdigitalsignature/IXpsSignatureBlock::GetPartName"]
old-location: xps\ixpssignatureblock_getpartname.htm
tech.root: xps
ms.assetid: 43dbb5f5-d69b-435e-8ace-54615796871d
ms.date: 12/05/2018
ms.keywords: GetPartName, GetPartName method [XPS Documents and Packaging], GetPartName method [XPS Documents and Packaging],IXpsSignatureBlock interface, IXpsSignatureBlock interface [XPS Documents and Packaging],GetPartName method, IXpsSignatureBlock.GetPartName, IXpsSignatureBlock::GetPartName, xps.ixpssignatureblock_getpartname, xpsdigitalsignature/IXpsSignatureBlock::GetPartName
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
 - IXpsSignatureBlock::GetPartName
 - xpsdigitalsignature/IXpsSignatureBlock::GetPartName
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
 - IXpsSignatureBlock.GetPartName
---

# IXpsSignatureBlock::GetPartName


## -description

Gets a pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the URI of the SignatureDefinitions part.

## -parameters

### -param partName [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the URI of the SignatureDefinitions part.

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
<i>partName</i> is <b>NULL</b>.

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