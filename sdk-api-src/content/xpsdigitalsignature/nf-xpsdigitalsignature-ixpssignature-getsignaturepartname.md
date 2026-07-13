---
UID: NF:xpsdigitalsignature.IXpsSignature.GetSignaturePartName
title: IXpsSignature::GetSignaturePartName (xpsdigitalsignature.h)
description: Gets the part name of the signature part.
helpviewer_keywords: ["GetSignaturePartName","GetSignaturePartName method [XPS Documents and Packaging]","GetSignaturePartName method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetSignaturePartName method","IXpsSignature.GetSignaturePartName","IXpsSignature::GetSignaturePartName","xps.ixpssignature_getsignaturepartname","xpsdigitalsignature/IXpsSignature::GetSignaturePartName"]
old-location: xps\ixpssignature_getsignaturepartname.htm
tech.root: xps
ms.assetid: ed0c29e2-225b-4478-a8d7-d9ec28f8b1f4
ms.date: 12/05/2018
ms.keywords: GetSignaturePartName, GetSignaturePartName method [XPS Documents and Packaging], GetSignaturePartName method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetSignaturePartName method, IXpsSignature.GetSignaturePartName, IXpsSignature::GetSignaturePartName, xps.ixpssignature_getsignaturepartname, xpsdigitalsignature/IXpsSignature::GetSignaturePartName
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
 - IXpsSignature::GetSignaturePartName
 - xpsdigitalsignature/IXpsSignature::GetSignaturePartName
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
 - IXpsSignature.GetSignaturePartName
---

# IXpsSignature::GetSignaturePartName


## -description

Gets the part name of the signature part.

## -parameters

### -param signaturePartName [out, retval]

A pointer to an  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the signature part.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>