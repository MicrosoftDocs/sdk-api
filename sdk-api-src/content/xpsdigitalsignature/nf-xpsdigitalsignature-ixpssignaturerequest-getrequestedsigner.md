---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetRequestedSigner
title: IXpsSignatureRequest::GetRequestedSigner (xpsdigitalsignature.h)
description: Gets the identity of the person who has signed or is requesting to sign the package.
helpviewer_keywords: ["GetRequestedSigner","GetRequestedSigner method [XPS Documents and Packaging]","GetRequestedSigner method [XPS Documents and Packaging]","IXpsSignatureRequest interface","IXpsSignatureRequest interface [XPS Documents and Packaging]","GetRequestedSigner method","IXpsSignatureRequest.GetRequestedSigner","IXpsSignatureRequest::GetRequestedSigner","xps.ixpssignaturerequest_getrequestedsigner","xpsdigitalsignature/IXpsSignatureRequest::GetRequestedSigner"]
old-location: xps\ixpssignaturerequest_getrequestedsigner.htm
tech.root: xps
ms.assetid: fbe5872e-76af-4aa1-86ad-ed7c36fd6447
ms.date: 12/05/2018
ms.keywords: GetRequestedSigner, GetRequestedSigner method [XPS Documents and Packaging], GetRequestedSigner method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetRequestedSigner method, IXpsSignatureRequest.GetRequestedSigner, IXpsSignatureRequest::GetRequestedSigner, xps.ixpssignaturerequest_getrequestedsigner, xpsdigitalsignature/IXpsSignatureRequest::GetRequestedSigner
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
 - IXpsSignatureRequest::GetRequestedSigner
 - xpsdigitalsignature/IXpsSignatureRequest::GetRequestedSigner
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
 - IXpsSignatureRequest.GetRequestedSigner
---

# IXpsSignatureRequest::GetRequestedSigner


## -description

Gets the identity of the person who has signed or is requesting to sign the package.

## -parameters

### -param signerName [out, retval]

The identity of the person who has signed or is requesting to sign the package.

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
<i>signerName</i> is <b>NULL</b>.

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

This method allocates the memory used by the string that is returned in <i>signerName</i>.  If <i>signerName</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>