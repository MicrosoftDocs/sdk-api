---
UID: NF:xpsdigitalsignature.IXpsSignatureBlock.CreateRequest
title: IXpsSignatureBlock::CreateRequest (xpsdigitalsignature.h)
description: Creates a new IXpsSignatureRequest interface and adds it to the signature block.
helpviewer_keywords: ["CreateRequest","CreateRequest method [XPS Documents and Packaging]","CreateRequest method [XPS Documents and Packaging]","IXpsSignatureBlock interface","IXpsSignatureBlock interface [XPS Documents and Packaging]","CreateRequest method","IXpsSignatureBlock.CreateRequest","IXpsSignatureBlock::CreateRequest","xps.ixpssignatureblock_createrequest","xpsdigitalsignature/IXpsSignatureBlock::CreateRequest"]
old-location: xps\ixpssignatureblock_createrequest.htm
tech.root: xps
ms.assetid: 73b9e0b4-a650-4886-bafb-828a659b8446
ms.date: 12/05/2018
ms.keywords: CreateRequest, CreateRequest method [XPS Documents and Packaging], CreateRequest method [XPS Documents and Packaging],IXpsSignatureBlock interface, IXpsSignatureBlock interface [XPS Documents and Packaging],CreateRequest method, IXpsSignatureBlock.CreateRequest, IXpsSignatureBlock::CreateRequest, xps.ixpssignatureblock_createrequest, xpsdigitalsignature/IXpsSignatureBlock::CreateRequest
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
 - IXpsSignatureBlock::CreateRequest
 - xpsdigitalsignature/IXpsSignatureBlock::CreateRequest
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
 - IXpsSignatureBlock.CreateRequest
---

# IXpsSignatureBlock::CreateRequest


## -description

Creates a new <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a> interface and adds it to the signature block.

## -parameters

### -param requestId [in]

A string that uniquely identifies the new signature request within the signature block. For the method to generate an ID string, set this parameter to <b>NULL</b>.

### -param signatureRequest [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a> interface. If access to the new request interface is not  required, this parameter can be set to <b>NULL</b>.

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
Either the interface is not connected to the signature manager, or <i>requestId</i> is <b>NULL</b> and a unique ID string could not be generated.

</td>
</tr>
</table>

## -remarks

The new signature request must have a unique request ID; no two  requests may have the same  ID string. 

Creating a new request marks the signature block as <i>dirty</i> and  generates new content for the SignatureDefinitions part. When the XPS package is serialized, the  new content will overwrite the previous content in the SignatureDefinitions part.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>