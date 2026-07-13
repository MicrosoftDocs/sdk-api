---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetSigningLocale
title: IXpsSignatureRequest::GetSigningLocale (xpsdigitalsignature.h)
description: Gets the legal jurisdiction of the package signing location.
helpviewer_keywords: ["GetSigningLocale","GetSigningLocale method [XPS Documents and Packaging]","GetSigningLocale method [XPS Documents and Packaging]","IXpsSignatureRequest interface","IXpsSignatureRequest interface [XPS Documents and Packaging]","GetSigningLocale method","IXpsSignatureRequest.GetSigningLocale","IXpsSignatureRequest::GetSigningLocale","xps.ixpssignaturerequest_getsigninglocale","xpsdigitalsignature/IXpsSignatureRequest::GetSigningLocale"]
old-location: xps\ixpssignaturerequest_getsigninglocale.htm
tech.root: xps
ms.assetid: 76b2d0a5-2d62-455d-8822-88ca14a497ae
ms.date: 12/05/2018
ms.keywords: GetSigningLocale, GetSigningLocale method [XPS Documents and Packaging], GetSigningLocale method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetSigningLocale method, IXpsSignatureRequest.GetSigningLocale, IXpsSignatureRequest::GetSigningLocale, xps.ixpssignaturerequest_getsigninglocale, xpsdigitalsignature/IXpsSignatureRequest::GetSigningLocale
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
 - IXpsSignatureRequest::GetSigningLocale
 - xpsdigitalsignature/IXpsSignatureRequest::GetSigningLocale
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
 - IXpsSignatureRequest.GetSigningLocale
---

# IXpsSignatureRequest::GetSigningLocale


## -description

Gets the legal jurisdiction of the package signing location.

## -parameters

### -param place [out, retval]

The legal jurisdiction of the package signing location

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
<i>place</i> is <b>NULL</b>.

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

This method allocates the memory used by the string that is returned in <i>place</i>.  If <i>place</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>