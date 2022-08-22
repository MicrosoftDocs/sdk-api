---
UID: NF:msopc.IOpcSigningOptions.SetSignatureId
title: IOpcSigningOptions::SetSignatureId (msopc.h)
description: Sets the value of the Id attribute of the Signature element. (IOpcSigningOptions.SetSignatureId)
helpviewer_keywords: ["IOpcSigningOptions interface [Open Packaging Conventions]","SetSignatureId method","IOpcSigningOptions.SetSignatureId","IOpcSigningOptions::SetSignatureId","SetSignatureId","SetSignatureId method [Open Packaging Conventions]","SetSignatureId method [Open Packaging Conventions]","IOpcSigningOptions interface","msopc/IOpcSigningOptions::SetSignatureId","opc.iopcsigningoptions_setsignatureid"]
old-location: opc\iopcsigningoptions_setsignatureid.htm
tech.root: OPC
ms.assetid: c723d6e8-6af3-41a2-b6dd-d26897495965
ms.date: 12/05/2018
ms.keywords: IOpcSigningOptions interface [Open Packaging Conventions],SetSignatureId method, IOpcSigningOptions.SetSignatureId, IOpcSigningOptions::SetSignatureId, SetSignatureId, SetSignatureId method [Open Packaging Conventions], SetSignatureId method [Open Packaging Conventions],IOpcSigningOptions interface, msopc/IOpcSigningOptions::SetSignatureId, opc.iopcsigningoptions_setsignatureid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcSigningOptions::SetSignatureId
 - msopc/IOpcSigningOptions::SetSignatureId
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
 - IOpcSigningOptions.SetSignatureId
---

# IOpcSigningOptions::SetSignatureId


## -description

Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.

## -parameters

### -param signatureId [in]

The value of the <b>Id</b> attribute.

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
The <i>signatureId</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>Id</b> attribute of the <b>Signature</b> element is optional. If this method is not called, the <b>Signature</b> element will not have the <b>Id</b> attribute.

To access the Id before the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignatureid">IOpcSigningOptions::GetSignatureId</a>.  To access the signature Id after the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignatureid">IOpcDigitalSignature::GetSignatureId</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
