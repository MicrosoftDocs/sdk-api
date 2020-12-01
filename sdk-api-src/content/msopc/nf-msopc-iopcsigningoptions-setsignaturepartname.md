---
UID: NF:msopc.IOpcSigningOptions.SetSignaturePartName
title: IOpcSigningOptions::SetSignaturePartName (msopc.h)
description: Sets the part name of the signature part where the signature markup will be stored.
helpviewer_keywords: ["IOpcSigningOptions interface [Open Packaging Conventions]","SetSignaturePartName method","IOpcSigningOptions.SetSignaturePartName","IOpcSigningOptions::SetSignaturePartName","SetSignaturePartName","SetSignaturePartName method [Open Packaging Conventions]","SetSignaturePartName method [Open Packaging Conventions]","IOpcSigningOptions interface","msopc/IOpcSigningOptions::SetSignaturePartName","opc.iopcsigningoptions_setsignaturepartname"]
old-location: opc\iopcsigningoptions_setsignaturepartname.htm
tech.root: OPC
ms.assetid: 36d69a11-bfc3-4f0a-a681-4e138751990d
ms.date: 12/05/2018
ms.keywords: IOpcSigningOptions interface [Open Packaging Conventions],SetSignaturePartName method, IOpcSigningOptions.SetSignaturePartName, IOpcSigningOptions::SetSignaturePartName, SetSignaturePartName, SetSignaturePartName method [Open Packaging Conventions], SetSignaturePartName method [Open Packaging Conventions],IOpcSigningOptions interface, msopc/IOpcSigningOptions::SetSignaturePartName, opc.iopcsigningoptions_setsignaturepartname
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcSigningOptions::SetSignaturePartName
 - msopc/IOpcSigningOptions::SetSignaturePartName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSigningOptions.SetSignaturePartName
---

# IOpcSigningOptions::SetSignaturePartName


## -description

Sets the part name of the signature part where the signature markup will be stored.

## -parameters

### -param signaturePartName [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the part name of the part where the signature markup is stored,  or <b>NULL</b> to generate a part name when the signature is created.

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
</table>

## -remarks

Until the signature is generated, the part name of the signature part that stores the signature markup can be changed. To set a new part name, call this method with the <i>signaturePartName</i> parameter value set to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the new name. To clear an existing part name, set the <i>signaturePartName</i> parameter value to <b>NULL</b>. 

To access the signature part name before the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturepartname">IOpcSigningOptions::GetSignaturePartName</a>.  To access the signature part name after the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturepartname">IOpcDigitalSignature::GetSignaturePartName</a> method.

The signature part that stores signature markup is specific to the signature.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>