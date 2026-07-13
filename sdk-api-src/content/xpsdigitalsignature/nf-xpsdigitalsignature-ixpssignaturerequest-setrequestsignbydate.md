---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.SetRequestSignByDate
title: IXpsSignatureRequest::SetRequestSignByDate (xpsdigitalsignature.h)
description: Sets the date and time before which the requested signer must sign the specified parts of the document.
helpviewer_keywords: ["IXpsSignatureRequest interface [XPS Documents and Packaging]","SetRequestSignByDate method","IXpsSignatureRequest.SetRequestSignByDate","IXpsSignatureRequest::SetRequestSignByDate","SetRequestSignByDate","SetRequestSignByDate method [XPS Documents and Packaging]","SetRequestSignByDate method [XPS Documents and Packaging]","IXpsSignatureRequest interface","xps.ixpssignaturerequest_setrequestsignbydate","xpsdigitalsignature/IXpsSignatureRequest::SetRequestSignByDate"]
old-location: xps\ixpssignaturerequest_setrequestsignbydate.htm
tech.root: xps
ms.assetid: b7048b34-17f8-4df4-b1c6-6c6e6250f02a
ms.date: 12/05/2018
ms.keywords: IXpsSignatureRequest interface [XPS Documents and Packaging],SetRequestSignByDate method, IXpsSignatureRequest.SetRequestSignByDate, IXpsSignatureRequest::SetRequestSignByDate, SetRequestSignByDate, SetRequestSignByDate method [XPS Documents and Packaging], SetRequestSignByDate method [XPS Documents and Packaging],IXpsSignatureRequest interface, xps.ixpssignaturerequest_setrequestsignbydate, xpsdigitalsignature/IXpsSignatureRequest::SetRequestSignByDate
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
 - IXpsSignatureRequest::SetRequestSignByDate
 - xpsdigitalsignature/IXpsSignatureRequest::SetRequestSignByDate
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
 - IXpsSignatureRequest.SetRequestSignByDate
---

# IXpsSignatureRequest::SetRequestSignByDate


## -description

Sets the date and time before which the requested signer must sign the specified parts of the document.

## -parameters

### -param dateString [in]

A string that contains the date and time before which the requested signer must sign the specified parts of the document.

The string must be formatted as <code>YYYY-MM-DDThh:mmZ</code> with the UTC time zone offset. For example, 7:30:29 A.M. Pacific Standard Time on July 4, 2008 would be represented as the UTC time of <code>2008-07-04T15:30:29Z</code>.

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

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>