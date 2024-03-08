---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.GetSignatureBlocks
title: IXpsSignatureManager::GetSignatureBlocks (xpsdigitalsignature.h)
description: Gets a pointer to an IXpsSignatureBlockCollection interface that contains a collection of signature blocks.
helpviewer_keywords: ["GetSignatureBlocks","GetSignatureBlocks method [XPS Documents and Packaging]","GetSignatureBlocks method [XPS Documents and Packaging]","IXpsSignatureManager interface","IXpsSignatureManager interface [XPS Documents and Packaging]","GetSignatureBlocks method","IXpsSignatureManager.GetSignatureBlocks","IXpsSignatureManager::GetSignatureBlocks","xps.ixpssignaturemanager_getsignatureblocks","xpsdigitalsignature/IXpsSignatureManager::GetSignatureBlocks"]
old-location: xps\ixpssignaturemanager_getsignatureblocks.htm
tech.root: xps
ms.assetid: 6f7ba22f-7c3b-47bf-8cb5-2e4e4a548dc2
ms.date: 12/05/2018
ms.keywords: GetSignatureBlocks, GetSignatureBlocks method [XPS Documents and Packaging], GetSignatureBlocks method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],GetSignatureBlocks method, IXpsSignatureManager.GetSignatureBlocks, IXpsSignatureManager::GetSignatureBlocks, xps.ixpssignaturemanager_getsignatureblocks, xpsdigitalsignature/IXpsSignatureManager::GetSignatureBlocks
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
 - IXpsSignatureManager::GetSignatureBlocks
 - xpsdigitalsignature/IXpsSignatureManager::GetSignatureBlocks
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
 - IXpsSignatureManager.GetSignatureBlocks
---

# IXpsSignatureManager::GetSignatureBlocks


## -description

Gets a pointer to an  <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a> interface that contains a collection of signature blocks.

## -parameters

### -param signatureBlocks [out, retval]

A pointer to an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a> interface that contains a collection of signature blocks.

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
<i>signatureBlocks</i> is <b>NULL</b>.

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

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection">IXpsSignatureBlockCollection</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>