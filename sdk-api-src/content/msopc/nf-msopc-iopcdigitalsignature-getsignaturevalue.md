---
UID: NF:msopc.IOpcDigitalSignature.GetSignatureValue
title: IOpcDigitalSignature::GetSignatureValue (msopc.h)
description: Gets the decoded value in the SignatureValue element of the signature markup.
helpviewer_keywords: ["GetSignatureValue","GetSignatureValue method [Open Packaging Conventions]","GetSignatureValue method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetSignatureValue method","IOpcDigitalSignature.GetSignatureValue","IOpcDigitalSignature::GetSignatureValue","msopc/IOpcDigitalSignature::GetSignatureValue","opc.iopcdigitalsignature_getsignaturevalue"]
old-location: opc\iopcdigitalsignature_getsignaturevalue.htm
tech.root: OPC
ms.assetid: c918d156-ad32-4a0c-83cc-dd37fe884744
ms.date: 12/05/2018
ms.keywords: GetSignatureValue, GetSignatureValue method [Open Packaging Conventions], GetSignatureValue method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignatureValue method, IOpcDigitalSignature.GetSignatureValue, IOpcDigitalSignature::GetSignatureValue, msopc/IOpcDigitalSignature::GetSignatureValue, opc.iopcdigitalsignature_getsignaturevalue
f1_keywords:
- msopc/IOpcDigitalSignature.GetSignatureValue
dev_langs:
- c++
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
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
- msopc.h
api_name:
- IOpcDigitalSignature.GetSignatureValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcDigitalSignature::GetSignatureValue


## -description


Gets the decoded value in the <b>SignatureValue</b> element of the signature markup.


## -parameters




### -param signatureValue [out]

A pointer to a buffer that contains the decoded value in the <b>SignatureValue</b> element of the signature markup.


### -param count [out]

The size of the <i>signatureHashValue</i> buffer.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
 At least one of the <i>signatureValue</i>, and <i>count</i> parameters is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates memory used by the buffer returned in <i>signatureValue</i>.  If the method succeeds, call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

The <b>SignatureValue</b> element contains a base-64 encoded value that was computed by applying the signature method to the <b>SignedInfo</b> element of the signature markup. To get the signature method, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturemethod">GetSignatureMethod</a> method.

When using the APIs to generate a signature, set the signature method by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturemethod">IOpcSigningOptions::SetSignatureMethod</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

