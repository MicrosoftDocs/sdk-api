---
UID: NF:msopc.IOpcDigitalSignatureManager.RemoveSignature
title: IOpcDigitalSignatureManager::RemoveSignature (msopc.h)
description: Removes from the package a specified signature part that stores signature markup.
helpviewer_keywords: ["IOpcDigitalSignatureManager interface [Open Packaging Conventions]","RemoveSignature method","IOpcDigitalSignatureManager.RemoveSignature","IOpcDigitalSignatureManager::RemoveSignature","RemoveSignature","RemoveSignature method [Open Packaging Conventions]","RemoveSignature method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","msopc/IOpcDigitalSignatureManager::RemoveSignature","opc.iopcdigitalsignaturemanager_removesignature"]
old-location: opc\iopcdigitalsignaturemanager_removesignature.htm
tech.root: OPC
ms.assetid: bc022b81-f61d-4efa-9c68-f798b2d929c2
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],RemoveSignature method, IOpcDigitalSignatureManager.RemoveSignature, IOpcDigitalSignatureManager::RemoveSignature, RemoveSignature, RemoveSignature method [Open Packaging Conventions], RemoveSignature method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::RemoveSignature, opc.iopcdigitalsignaturemanager_removesignature
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
 - IOpcDigitalSignatureManager::RemoveSignature
 - msopc/IOpcDigitalSignatureManager::RemoveSignature
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
 - IOpcDigitalSignatureManager.RemoveSignature
---

# IOpcDigitalSignatureManager::RemoveSignature


## -description

Removes from the package a specified signature part  that stores signature markup.

## -parameters

### -param signaturePartName [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the part name of the signature part to be removed.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NO_SUCH_PART</b></dt>
<dt>0x80510018</dt>
</dl>
</td>
<td width="60%">
The specified part does not exist.

</td>
</tr>
</table>

## -remarks

If the specified signature part does not exist, this method will fail.

If a part is removed from a package, it will not be saved when the package is saved.

If a removed part is the source of one or more relationships, those relationships will not be saved when the package is saved.


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