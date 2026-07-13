---
UID: NF:xpsdigitalsignature.IXpsSignatureRequest.SetIntent
title: IXpsSignatureRequest::SetIntent (xpsdigitalsignature.h)
description: Sets the string that describes the intent or meaning of the signature. (IXpsSignatureRequest.SetIntent)
helpviewer_keywords: ["IXpsSignatureRequest interface [XPS Documents and Packaging]","SetIntent method","IXpsSignatureRequest.SetIntent","IXpsSignatureRequest::SetIntent","SetIntent","SetIntent method [XPS Documents and Packaging]","SetIntent method [XPS Documents and Packaging]","IXpsSignatureRequest interface","xps.ixpssignaturerequest_setintent","xpsdigitalsignature/IXpsSignatureRequest::SetIntent"]
old-location: xps\ixpssignaturerequest_setintent.htm
tech.root: xps
ms.assetid: 8a77a168-58c7-4bb4-83ee-ed4dfd2839fe
ms.date: 12/05/2018
ms.keywords: IXpsSignatureRequest interface [XPS Documents and Packaging],SetIntent method, IXpsSignatureRequest.SetIntent, IXpsSignatureRequest::SetIntent, SetIntent, SetIntent method [XPS Documents and Packaging], SetIntent method [XPS Documents and Packaging],IXpsSignatureRequest interface, xps.ixpssignaturerequest_setintent, xpsdigitalsignature/IXpsSignatureRequest::SetIntent
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
 - IXpsSignatureRequest::SetIntent
 - xpsdigitalsignature/IXpsSignatureRequest::SetIntent
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
 - IXpsSignatureRequest.SetIntent
---

# IXpsSignatureRequest::SetIntent


## -description

Sets the string that describes the intent or meaning of the signature.

## -parameters

### -param intent [in]

The string that describes the intent or meaning of the signature.

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
<i>intent</i> is <b>NULL</b>.

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

The signature intent string describes what the signature means to the signer. For example, for the  signature intent string "I have read and agree with the contents of this document" the presence of a digital signature means that the signer has read and agrees with the content of the document.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest">IXpsSignatureRequest</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
