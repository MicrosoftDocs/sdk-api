---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.AddSignatureBlock
title: IXpsSignatureManager::AddSignatureBlock (xpsdigitalsignature.h)
description: Creates a new IXpsSignatureBlock interface and adds it to the signature block collection.
helpviewer_keywords: ["AddSignatureBlock","AddSignatureBlock method [XPS Documents and Packaging]","AddSignatureBlock method [XPS Documents and Packaging]","IXpsSignatureManager interface","IXpsSignatureManager interface [XPS Documents and Packaging]","AddSignatureBlock method","IXpsSignatureManager.AddSignatureBlock","IXpsSignatureManager::AddSignatureBlock","xps.ixpssignaturemanager_addsignatureblock","xpsdigitalsignature/IXpsSignatureManager::AddSignatureBlock"]
old-location: xps\ixpssignaturemanager_addsignatureblock.htm
tech.root: xps
ms.assetid: a299882f-b9f4-4297-8438-e92d148a4014
ms.date: 12/05/2018
ms.keywords: AddSignatureBlock, AddSignatureBlock method [XPS Documents and Packaging], AddSignatureBlock method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],AddSignatureBlock method, IXpsSignatureManager.AddSignatureBlock, IXpsSignatureManager::AddSignatureBlock, xps.ixpssignaturemanager_addsignatureblock, xpsdigitalsignature/IXpsSignatureManager::AddSignatureBlock
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
 - IXpsSignatureManager::AddSignatureBlock
 - xpsdigitalsignature/IXpsSignatureManager::AddSignatureBlock
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
 - IXpsSignatureManager.AddSignatureBlock
---

# IXpsSignatureManager::AddSignatureBlock


## -description

Creates a new <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface and adds it to the signature block collection.

## -parameters

### -param partName [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the URI of the new part. For the method to generate a part name, this parameter can be set to <b>NULL</b>.

### -param fixedDocumentIndex [in]

The index value of the FixedDocument part with which the new signature block is to be associated.

### -param signatureBlock [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface. If access to the new interface is not required, this parameter can be set to <b>NULL</b>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>fixedDocumentIndex</i> references a fixed document that is not found in the XPS package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has not yet been opened in the signature manager.

</td>
</tr>
</table>

## -remarks

A signature block represents a SignatureDefinitions part in an XPS package. According to section 10.2.2 in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>,  zero or more SignatureDefinitions parts can be attached to each FixedDocument.
     This method creates a new SignatureDefinitions part with the specified name,   links it from the specified FixedDocument part by a relationship, 
    creates a new  <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface, and adds this new  interface to the internal signature block collection.

To retrieve a signature block, call   the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatureblocks">GetSignatureBlocks</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>