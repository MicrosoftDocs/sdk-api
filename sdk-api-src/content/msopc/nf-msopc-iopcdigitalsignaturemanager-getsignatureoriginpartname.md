---
UID: NF:msopc.IOpcDigitalSignatureManager.GetSignatureOriginPartName
title: IOpcDigitalSignatureManager::GetSignatureOriginPartName (msopc.h)
description: Gets an IOpcPartUri interface pointer that represents the part name of the Digital Signature Origin part.
helpviewer_keywords: ["GetSignatureOriginPartName","GetSignatureOriginPartName method [Open Packaging Conventions]","GetSignatureOriginPartName method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","IOpcDigitalSignatureManager interface [Open Packaging Conventions]","GetSignatureOriginPartName method","IOpcDigitalSignatureManager.GetSignatureOriginPartName","IOpcDigitalSignatureManager::GetSignatureOriginPartName","msopc/IOpcDigitalSignatureManager::GetSignatureOriginPartName","opc.iopcdigitalsignaturemanager_getsignatureoriginpartname"]
old-location: opc\iopcdigitalsignaturemanager_getsignatureoriginpartname.htm
tech.root: OPC
ms.assetid: 958cf2e7-0956-489a-904f-01ec00af48d1
ms.date: 12/05/2018
ms.keywords: GetSignatureOriginPartName, GetSignatureOriginPartName method [Open Packaging Conventions], GetSignatureOriginPartName method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, IOpcDigitalSignatureManager interface [Open Packaging Conventions],GetSignatureOriginPartName method, IOpcDigitalSignatureManager.GetSignatureOriginPartName, IOpcDigitalSignatureManager::GetSignatureOriginPartName, msopc/IOpcDigitalSignatureManager::GetSignatureOriginPartName, opc.iopcdigitalsignaturemanager_getsignatureoriginpartname
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
 - IOpcDigitalSignatureManager::GetSignatureOriginPartName
 - msopc/IOpcDigitalSignatureManager::GetSignatureOriginPartName
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
 - IOpcDigitalSignatureManager.GetSignatureOriginPartName
---

# IOpcDigitalSignatureManager::GetSignatureOriginPartName


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the part name of the Digital Signature Origin part.

## -parameters

### -param signatureOriginPartName [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer, or <b>NULL</b> if the Digital Signature Origin part does not exist.

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
The <i>signatureOriginPartName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

When using the APIs to generate a signature, set the Digital Signature Origin part name  by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-setsignatureoriginpartname">SetSignatureOriginPartName</a> method.


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