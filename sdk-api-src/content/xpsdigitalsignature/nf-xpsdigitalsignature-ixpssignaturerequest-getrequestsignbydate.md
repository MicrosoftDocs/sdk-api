---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetRequestSignByDate
title: IXpsSignatureRequest::GetRequestSignByDate (xpsdigitalsignature.h)
description: Gets the date and time before which the requested signer must sign the specified parts of the document.
helpviewer_keywords: ["GetRequestSignByDate","GetRequestSignByDate method [XPS Documents and Packaging]","GetRequestSignByDate method [XPS Documents and Packaging]","IXpsSignatureRequest interface","IXpsSignatureRequest interface [XPS Documents and Packaging]","GetRequestSignByDate method","IXpsSignatureRequest.GetRequestSignByDate","IXpsSignatureRequest::GetRequestSignByDate","xps.ixpssignaturerequest_getrequestsignbydate","xpsdigitalsignature/IXpsSignatureRequest::GetRequestSignByDate"]
old-location: xps\ixpssignaturerequest_getrequestsignbydate.htm
tech.root: xps
ms.assetid: 14cbe79d-a299-4e8d-9734-8571c0b535ce
ms.date: 12/05/2018
ms.keywords: GetRequestSignByDate, GetRequestSignByDate method [XPS Documents and Packaging], GetRequestSignByDate method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetRequestSignByDate method, IXpsSignatureRequest.GetRequestSignByDate, IXpsSignatureRequest::GetRequestSignByDate, xps.ixpssignaturerequest_getrequestsignbydate, xpsdigitalsignature/IXpsSignatureRequest::GetRequestSignByDate
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
 - IXpsSignatureRequest::GetRequestSignByDate
 - xpsdigitalsignature/IXpsSignatureRequest::GetRequestSignByDate
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
 - IXpsSignatureRequest.GetRequestSignByDate
---

# IXpsSignatureRequest::GetRequestSignByDate


## -description

Gets the date and time before which the requested signer must sign the specified parts of the document.

## -parameters

### -param dateString [out, retval]

A string that contains the date and time before which the requested signer must sign the specified parts of the document.

The string is formatted as either <code>YYYY-MM-DDThh:mmZ</code>,  which includes the UTC time zone offset, or <code>YYYY-MM-DDThh:mm</code>, which does not include the UTC time zone offset. For example, without the time zone offset, 7:30:29 P.M. on July 4, 2008 would be represented  as <code>2008-07-04T19:30:29</code>.

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
<i>dateString</i> is <b>NULL</b>.

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

This method allocates the memory used by the string that is returned in <i>dateString</i>.  If <i>dateString</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>