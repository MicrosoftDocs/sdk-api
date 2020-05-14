---
UID: NF:msopc.IOpcSigningOptions.GetSignaturePartName
title: IOpcSigningOptions::GetSignaturePartName (msopc.h)
description: Gets the part name of the signature part where the signature markup will be stored.helpviewer_keywords: ["GetSignaturePartName","GetSignaturePartName method [Open Packaging Conventions]","GetSignaturePartName method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetSignaturePartName method","IOpcSigningOptions.GetSignaturePartName","IOpcSigningOptions::GetSignaturePartName","msopc/IOpcSigningOptions::GetSignaturePartName","opc.iopcsigningoptions_getsignaturepartname"]
old-location: opc\iopcsigningoptions_getsignaturepartname.htm
tech.root: OPC
ms.assetid: 09481639-eea1-4203-932f-e97558408b42
ms.date: 12/05/2018
ms.keywords: GetSignaturePartName, GetSignaturePartName method [Open Packaging Conventions], GetSignaturePartName method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetSignaturePartName method, IOpcSigningOptions.GetSignaturePartName, IOpcSigningOptions::GetSignaturePartName, msopc/IOpcSigningOptions::GetSignaturePartName, opc.iopcsigningoptions_getsignaturepartname
f1_keywords:
- msopc/IOpcSigningOptions.GetSignaturePartName
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
req.idl: Msopc.idl
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
- IOpcSigningOptions.GetSignaturePartName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcSigningOptions::GetSignaturePartName


## -description


Gets the part name of the signature part where the signature markup will be stored.


## -parameters




### -param signaturePartName [out, retval]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the part name of the part where the signature markup is stored,  or <b>NULL</b> if the part name  has not been set by a call to  the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturepartname">SetSignaturePartName</a> method.


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
The <i>signaturePartName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To set the part name of the signature part that stores the signature markup, call  the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturepartname">IOpcSigningOptions::SetSignaturePartName</a> method.

To access the signature part name after the signature is generated, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturepartname">IOpcDigitalSignature::GetSignaturePartName</a> method.

The signature part that stores signature markup is specific to the signature.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



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
 

 

