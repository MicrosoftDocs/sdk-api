---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.GetSignatures
title: IXpsSignatureManager::GetSignatures (xpsdigitalsignature.h)
description: Gets a pointer to an IXpsSignatureCollection interface that contains a collection of XPS digital signatures.
helpviewer_keywords: ["GetSignatures","GetSignatures method [XPS Documents and Packaging]","GetSignatures method [XPS Documents and Packaging]","IXpsSignatureManager interface","IXpsSignatureManager interface [XPS Documents and Packaging]","GetSignatures method","IXpsSignatureManager.GetSignatures","IXpsSignatureManager::GetSignatures","xps.ixpssignaturemanager_getsignatures","xpsdigitalsignature/IXpsSignatureManager::GetSignatures"]
old-location: xps\ixpssignaturemanager_getsignatures.htm
tech.root: xps
ms.assetid: 3a6a9a10-bc1d-45b8-a1b9-c7b725d9c13b
ms.date: 12/05/2018
ms.keywords: GetSignatures, GetSignatures method [XPS Documents and Packaging], GetSignatures method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],GetSignatures method, IXpsSignatureManager.GetSignatures, IXpsSignatureManager::GetSignatures, xps.ixpssignaturemanager_getsignatures, xpsdigitalsignature/IXpsSignatureManager::GetSignatures
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
 - IXpsSignatureManager::GetSignatures
 - xpsdigitalsignature/IXpsSignatureManager::GetSignatures
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
 - IXpsSignatureManager.GetSignatures
---

# IXpsSignatureManager::GetSignatures


## -description

Gets a pointer to an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection">IXpsSignatureCollection</a> interface that contains a collection of XPS digital signatures.

## -parameters

### -param signatures [out, retval]

A pointer to an <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection">IXpsSignatureCollection</a> interface that contains a collection of XPS digital signatures.

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
<i>signatures</i> is <b>NULL</b>.

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

The signature collection that is returned in <i>signatures</i> might include digital signatures that do not comply with the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection">IXpsSignatureCollection</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>