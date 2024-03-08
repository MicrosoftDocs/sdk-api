---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.GetSignatureOriginPartName
title: IXpsSignatureManager::GetSignatureOriginPartName (xpsdigitalsignature.h)
description: Gets the part name of the signature origin part.
helpviewer_keywords: ["GetSignatureOriginPartName","GetSignatureOriginPartName method [XPS Documents and Packaging]","GetSignatureOriginPartName method [XPS Documents and Packaging]","IXpsSignatureManager interface","IXpsSignatureManager interface [XPS Documents and Packaging]","GetSignatureOriginPartName method","IXpsSignatureManager.GetSignatureOriginPartName","IXpsSignatureManager::GetSignatureOriginPartName","xps.ixpssignaturemanager_getsignatureoriginpartname","xpsdigitalsignature/IXpsSignatureManager::GetSignatureOriginPartName"]
old-location: xps\ixpssignaturemanager_getsignatureoriginpartname.htm
tech.root: xps
ms.assetid: 0d70e6bc-1101-40fa-b91c-69facc3ca195
ms.date: 12/05/2018
ms.keywords: GetSignatureOriginPartName, GetSignatureOriginPartName method [XPS Documents and Packaging], GetSignatureOriginPartName method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],GetSignatureOriginPartName method, IXpsSignatureManager.GetSignatureOriginPartName, IXpsSignatureManager::GetSignatureOriginPartName, xps.ixpssignaturemanager_getsignatureoriginpartname, xpsdigitalsignature/IXpsSignatureManager::GetSignatureOriginPartName
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
 - IXpsSignatureManager::GetSignatureOriginPartName
 - xpsdigitalsignature/IXpsSignatureManager::GetSignatureOriginPartName
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
 - IXpsSignatureManager.GetSignatureOriginPartName
---

# IXpsSignatureManager::GetSignatureOriginPartName


## -description

Gets the part name of the signature origin part.

## -parameters

### -param signatureOriginPartName [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the signature origin part. If the document does not have any signatures, a <b>NULL</b> pointer is returned.

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
<dt><b>XPS_E_PACKAGE_NOT_OPENED</b></dt>
</dl>
</td>
<td width="60%">
An XPS package has not yet been opened in the signature manager.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>