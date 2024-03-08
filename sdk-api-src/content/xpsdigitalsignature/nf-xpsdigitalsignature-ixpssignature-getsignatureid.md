---
UID: NF:xpsdigitalsignature.IXpsSignature.GetSignatureId
title: IXpsSignature::GetSignatureId (xpsdigitalsignature.h)
description: Gets the value of the Id attribute of the Signature element. (IXpsSignature.GetSignatureId)
helpviewer_keywords: ["GetSignatureId","GetSignatureId method [XPS Documents and Packaging]","GetSignatureId method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetSignatureId method","IXpsSignature.GetSignatureId","IXpsSignature::GetSignatureId","xps.ixpssignature_getsignatureid","xpsdigitalsignature/IXpsSignature::GetSignatureId"]
old-location: xps\ixpssignature_getsignatureid.htm
tech.root: xps
ms.assetid: 9debed66-6588-40b5-ab52-a3dba0ddef92
ms.date: 12/05/2018
ms.keywords: GetSignatureId, GetSignatureId method [XPS Documents and Packaging], GetSignatureId method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetSignatureId method, IXpsSignature.GetSignatureId, IXpsSignature::GetSignatureId, xps.ixpssignature_getsignatureid, xpsdigitalsignature/IXpsSignature::GetSignatureId
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
 - IXpsSignature::GetSignatureId
 - xpsdigitalsignature/IXpsSignature::GetSignatureId
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
 - IXpsSignature.GetSignatureId
---

# IXpsSignature::GetSignatureId


## -description

Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

## -parameters

### -param sigId [out, retval]

The value of the <b>Id</b> attribute of the <b>Signature</b> element. If the <b>Id</b> attribute is not present, a <b>NULL</b> pointer is returned.

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
<i>sigId</i> is <b>NULL</b>.

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

This method allocates the memory used by the string that is returned in <i>sigId</i>.  If <i>sigId</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
