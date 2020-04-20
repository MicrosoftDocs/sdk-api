---
UID: NF:xpsdigitalsignature.IXpsSignature.GetSignatureValue
title: IXpsSignature::GetSignatureValue (xpsdigitalsignature.h)
description: Gets the encrypted hash value of the signature.helpviewer_keywords: ["GetSignatureValue","GetSignatureValue method [XPS Documents and Packaging]","GetSignatureValue method [XPS Documents and Packaging]","IXpsSignature interface","IXpsSignature interface [XPS Documents and Packaging]","GetSignatureValue method","IXpsSignature.GetSignatureValue","IXpsSignature::GetSignatureValue","xps.ixpssignature_getsignaturevalue","xpsdigitalsignature/IXpsSignature::GetSignatureValue"]
old-location: xps\ixpssignature_getsignaturevalue.htm
tech.root: printdocs
ms.assetid: 40a21fa3-cf71-4c0d-8343-83a2c1a216c9
ms.date: 12/05/2018
ms.keywords: GetSignatureValue, GetSignatureValue method [XPS Documents and Packaging], GetSignatureValue method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetSignatureValue method, IXpsSignature.GetSignatureValue, IXpsSignature::GetSignatureValue, xps.ixpssignature_getsignaturevalue, xpsdigitalsignature/IXpsSignature::GetSignatureValue
f1_keywords:
- xpsdigitalsignature/IXpsSignature.GetSignatureValue
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
- IXpsSignature.GetSignatureValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSignature::GetSignatureValue


## -description


Gets the encrypted hash value of the signature.


## -parameters




### -param signatureHashValue [out]

The byte array that represents the encrypted hash value of the signature.


### -param count [out]

The length of the byte array that is referenced by <i>signatureHashValue</i>.




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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface is not connected to the signature manager.

</td>
</tr>
</table>
 




## -remarks



This method allocates the memory buffer whose pointer is returned in <i>signatureHashValue</i>.  If <i>signatureHashValue</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature">IXpsSignature</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager">IXpsSignatureManager</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372949(v=vs.85)">XPS Digital Signature API Errors</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

