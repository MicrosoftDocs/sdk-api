---
UID: NF:msopc.IOpcDigitalSignatureManager.CreateSigningOptions
title: IOpcDigitalSignatureManager::CreateSigningOptions (msopc.h)
description: Creates an IOpcSigningOptions interface pointer.
helpviewer_keywords: ["CreateSigningOptions","CreateSigningOptions method [Open Packaging Conventions]","CreateSigningOptions method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","IOpcDigitalSignatureManager interface [Open Packaging Conventions]","CreateSigningOptions method","IOpcDigitalSignatureManager.CreateSigningOptions","IOpcDigitalSignatureManager::CreateSigningOptions","msopc/IOpcDigitalSignatureManager::CreateSigningOptions","opc.iopcdigitalsignaturemanager_createsigningoptions"]
old-location: opc\iopcdigitalsignaturemanager_createsigningoptions.htm
tech.root: OPC
ms.assetid: c58f9730-b2c2-40cd-8aae-03fbd09f8c76
ms.date: 12/05/2018
ms.keywords: CreateSigningOptions, CreateSigningOptions method [Open Packaging Conventions], CreateSigningOptions method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, IOpcDigitalSignatureManager interface [Open Packaging Conventions],CreateSigningOptions method, IOpcDigitalSignatureManager.CreateSigningOptions, IOpcDigitalSignatureManager::CreateSigningOptions, msopc/IOpcDigitalSignatureManager::CreateSigningOptions, opc.iopcdigitalsignaturemanager_createsigningoptions
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
 - IOpcDigitalSignatureManager::CreateSigningOptions
 - msopc/IOpcDigitalSignatureManager::CreateSigningOptions
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
 - IOpcDigitalSignatureManager.CreateSigningOptions
---

# IOpcDigitalSignatureManager::CreateSigningOptions


## -description

Creates an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer.

## -parameters

### -param signingOptions [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer.

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
The <i>signingOptions</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method creates an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer that is required to set the properties of a signature to be generated

To generate a signature, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignatureManager::Sign</a> method with the <i>signingOptions</i> parameter value set to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer that is retrieved by the <b>CreateSigningOptions</b> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>