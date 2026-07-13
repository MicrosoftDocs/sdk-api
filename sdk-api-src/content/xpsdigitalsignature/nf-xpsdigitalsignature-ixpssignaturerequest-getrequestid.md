---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.GetRequestId
title: IXpsSignatureRequest::GetRequestId (xpsdigitalsignature.h)
description: Gets the unique identifier of the signature request.
helpviewer_keywords: ["GetRequestId","GetRequestId method [XPS Documents and Packaging]","GetRequestId method [XPS Documents and Packaging]","IXpsSignatureRequest interface","IXpsSignatureRequest interface [XPS Documents and Packaging]","GetRequestId method","IXpsSignatureRequest.GetRequestId","IXpsSignatureRequest::GetRequestId","xps.ixpssignaturerequest_getrequestid","xpsdigitalsignature/IXpsSignatureRequest::GetRequestId"]
old-location: xps\ixpssignaturerequest_getrequestid.htm
tech.root: xps
ms.assetid: abca5fdf-258b-4ce8-8b29-eae9a6d17cd7
ms.date: 12/05/2018
ms.keywords: GetRequestId, GetRequestId method [XPS Documents and Packaging], GetRequestId method [XPS Documents and Packaging],IXpsSignatureRequest interface, IXpsSignatureRequest interface [XPS Documents and Packaging],GetRequestId method, IXpsSignatureRequest.GetRequestId, IXpsSignatureRequest::GetRequestId, xps.ixpssignaturerequest_getrequestid, xpsdigitalsignature/IXpsSignatureRequest::GetRequestId
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
 - IXpsSignatureRequest::GetRequestId
 - xpsdigitalsignature/IXpsSignatureRequest::GetRequestId
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
 - IXpsSignatureRequest.GetRequestId
---

# IXpsSignatureRequest::GetRequestId


## -description

Gets the unique identifier of  the signature request.

## -parameters

### -param requestId [out, retval]

The unique identifier of  the signature request.

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
<i>requestId</i> is <b>NULL</b>.

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

This method allocates the memory used by the string that is returned in <i>requestId</i>.  If <i>requestId</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

 The <i>requestId</i> parameter receives the value of the <b>SpotID</b> attribute  of the <b>SignatureDefinition</b> element. The <b>SpotID</b> attribute  is required and should follow the xs:ID (XML ID) format; however, 
    existing SignatureDefinitions parts are not checked for adherence to the recommended format. Some XPS documents that were produced by Windows Presentation Foundation (WPF) applications may have an ID that starts with a digit.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>