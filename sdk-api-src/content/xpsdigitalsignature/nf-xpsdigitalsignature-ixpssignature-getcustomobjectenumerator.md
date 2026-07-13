---
UID: NF:xpsdigitalsignature.IXpsSignature.GetCustomObjectEnumerator
title: IXpsSignature::GetCustomObjectEnumerator (xpsdigitalsignature.h)
description: Gets a pointer to an IOpcSignatureCustomObjectEnumerator interface, which enumerates the custom objects of the signature.
helpviewer_keywords: ["GetCustomObjectEnumerator","GetCustomObjectEnumerator method [XPS Documents and Packaging]","GetCustomObjectEnumerator method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetCustomObjectEnumerator method","IXpsSignature.GetCustomObjectEnumerator","IXpsSignature::GetCustomObjectEnumerator","xps.ixpssignature_getcustomobjectenumerator","xpsdigitalsignature/IXpsSignature::GetCustomObjectEnumerator"]
old-location: xps\ixpssignature_getcustomobjectenumerator.htm
tech.root: xps
ms.assetid: 98a656c7-714b-4b59-9289-e78dee795eaa
ms.date: 12/05/2018
ms.keywords: GetCustomObjectEnumerator, GetCustomObjectEnumerator method [XPS Documents and Packaging], GetCustomObjectEnumerator method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetCustomObjectEnumerator method, IXpsSignature.GetCustomObjectEnumerator, IXpsSignature::GetCustomObjectEnumerator, xps.ixpssignature_getcustomobjectenumerator, xpsdigitalsignature/IXpsSignature::GetCustomObjectEnumerator
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
 - IXpsSignature::GetCustomObjectEnumerator
 - xpsdigitalsignature/IXpsSignature::GetCustomObjectEnumerator
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
 - IXpsSignature.GetCustomObjectEnumerator
---

# IXpsSignature::GetCustomObjectEnumerator


## -description

Gets a pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectenumerator">IOpcSignatureCustomObjectEnumerator</a> interface, which enumerates the custom objects of the signature.

## -parameters

### -param customObjectEnumerator [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface, which  enumerates the custom objects of the signature.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not connected to the signature manager.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_OBJECT_DETACHED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not associated with the signature manager.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>