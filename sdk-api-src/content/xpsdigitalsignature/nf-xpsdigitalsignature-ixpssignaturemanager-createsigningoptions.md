---
UID: NF:xpsdigitalsignature.IXpsSignatureManager.CreateSigningOptions
title: IXpsSignatureManager::CreateSigningOptions (xpsdigitalsignature.h)
description: Creates a new IXpsSigningOptions interface.
helpviewer_keywords: ["CreateSigningOptions","CreateSigningOptions method [XPS Documents and Packaging]","CreateSigningOptions method [XPS Documents and Packaging]","IXpsSignatureManager interface","IXpsSignatureManager interface [XPS Documents and Packaging]","CreateSigningOptions method","IXpsSignatureManager.CreateSigningOptions","IXpsSignatureManager::CreateSigningOptions","xps.ixpssignaturemanager_createsigningoptions","xpsdigitalsignature/IXpsSignatureManager::CreateSigningOptions"]
old-location: xps\ixpssignaturemanager_createsigningoptions.htm
tech.root: xps
ms.assetid: 0f64f46a-905a-48cf-9e7a-f6cc1b2d6450
ms.date: 12/05/2018
ms.keywords: CreateSigningOptions, CreateSigningOptions method [XPS Documents and Packaging], CreateSigningOptions method [XPS Documents and Packaging],IXpsSignatureManager interface, IXpsSignatureManager interface [XPS Documents and Packaging],CreateSigningOptions method, IXpsSignatureManager.CreateSigningOptions, IXpsSignatureManager::CreateSigningOptions, xps.ixpssignaturemanager_createsigningoptions, xpsdigitalsignature/IXpsSignatureManager::CreateSigningOptions
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
 - IXpsSignatureManager::CreateSigningOptions
 - xpsdigitalsignature/IXpsSignatureManager::CreateSigningOptions
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
 - IXpsSignatureManager.CreateSigningOptions
---

# IXpsSignatureManager::CreateSigningOptions


## -description

Creates a new  <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface.

## -parameters

### -param signingOptions [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface.

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
<i>signingOptions</i> is <b>NULL</b>.

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

The new  <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface can be used to set the signing options for the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method; however, the SignatureMethod and the DigestMethod  properties must be initialized before the new interface  can be used as a parameter of the <b>Sign</b> method.

The <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a> interface created by this method can be used in more than one call to the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>