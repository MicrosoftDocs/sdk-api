---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetSignature
title: IXpsSignatureRequest::GetSignature (xpsdigitalsignature.h)
description: Gets a pointer to an IXpsSignature interface that contains the XPS digital signature with the same unique identifier as the signature request.helpviewer_keywords: ["GetSignature","GetSignature method [XPS Documents and Packaging]","GetSignature method [XPS Documents and Packaging]","IXpsSignatureRequest interface","IXpsSignatureRequest interface [XPS Documents and Packaging]","GetSignature method","IXpsSignatureRequest.GetSignature","IXpsSignatureRequest::GetSignature","xps.ixpssignaturerequest_getsignature","xpsdigitalsignature/IXpsSignatureRequest::GetSignature"]
old-location: xps\ixpssignaturerequest_getsignature.htm
tech.root: printdocs
ms.assetid: 649ab92f-9195-47a9-8a02-546825245e2b
ms.date: 12/05/2018
ms.keywords: GetSignature, GetSignature method [XPS Documents and Packaging], GetSignature method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetSignature method, IXpsSignatureRequest.GetSignature, IXpsSignatureRequest::GetSignature, xps.ixpssignaturerequest_getsignature, xpsdigitalsignature/IXpsSignatureRequest::GetSignature
f1_keywords:
- xpsdigitalsignature/IXpsSignatureRequest.GetSignature
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsdigitalsignature.h
api_name:
- IXpsSignatureRequest.GetSignature
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSignatureRequest::GetSignature


## -description


Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a> interface that contains the XPS digital signature with the same unique identifier as the signature request.


## -parameters




### -param signature [out, retval]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a> interface that contains the XPS digital signature with the same unique identifier as the signature request. If no matching signature is found, a <b>NULL</b> pointer is returned.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a> and  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>signature</i> is <b>NULL</b>.

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




<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

