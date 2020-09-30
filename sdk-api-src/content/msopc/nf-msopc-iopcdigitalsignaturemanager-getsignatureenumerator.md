---
UID: NF:msopc.IOpcDigitalSignatureManager.GetSignatureEnumerator
title: IOpcDigitalSignatureManager::GetSignatureEnumerator (msopc.h)
description: Gets an enumerator of IOpcDigitalSignature interface pointers, which represent package signatures.
helpviewer_keywords: ["GetSignatureEnumerator","GetSignatureEnumerator method [Open Packaging Conventions]","GetSignatureEnumerator method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","IOpcDigitalSignatureManager interface [Open Packaging Conventions]","GetSignatureEnumerator method","IOpcDigitalSignatureManager.GetSignatureEnumerator","IOpcDigitalSignatureManager::GetSignatureEnumerator","msopc/IOpcDigitalSignatureManager::GetSignatureEnumerator","opc.iopcdigitalsignaturemanager_getsignatureenumerator"]
old-location: opc\iopcdigitalsignaturemanager_getsignatureenumerator.htm
tech.root: OPC
ms.assetid: 44906f03-806f-400c-a7f3-0da5c330e1ff
ms.date: 12/05/2018
ms.keywords: GetSignatureEnumerator, GetSignatureEnumerator method [Open Packaging Conventions], GetSignatureEnumerator method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, IOpcDigitalSignatureManager interface [Open Packaging Conventions],GetSignatureEnumerator method, IOpcDigitalSignatureManager.GetSignatureEnumerator, IOpcDigitalSignatureManager::GetSignatureEnumerator, msopc/IOpcDigitalSignatureManager::GetSignatureEnumerator, opc.iopcdigitalsignaturemanager_getsignatureenumerator
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
 - IOpcDigitalSignatureManager::GetSignatureEnumerator
 - msopc/IOpcDigitalSignatureManager::GetSignatureEnumerator
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
 - IOpcDigitalSignatureManager.GetSignatureEnumerator
---

# IOpcDigitalSignatureManager::GetSignatureEnumerator


## -description

Gets an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointers, which represent package signatures.

## -parameters

### -param signatureEnumerator [out, retval]

A pointer to  an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointers, which represent package signatures.

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
The <i>signatureEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignatureenumerator">IOpcDigitalSignatureEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>