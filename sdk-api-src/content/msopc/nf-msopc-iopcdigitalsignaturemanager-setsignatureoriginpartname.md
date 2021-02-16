---
UID: NF:msopc.IOpcDigitalSignatureManager.SetSignatureOriginPartName
title: IOpcDigitalSignatureManager::SetSignatureOriginPartName (msopc.h)
description: Sets the part name of the Digital Signature Origin part to the name represented by a specified IOpcPartUri interface pointer.
helpviewer_keywords: ["IOpcDigitalSignatureManager interface [Open Packaging Conventions]","SetSignatureOriginPartName method","IOpcDigitalSignatureManager.SetSignatureOriginPartName","IOpcDigitalSignatureManager::SetSignatureOriginPartName","SetSignatureOriginPartName","SetSignatureOriginPartName method [Open Packaging Conventions]","SetSignatureOriginPartName method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","msopc/IOpcDigitalSignatureManager::SetSignatureOriginPartName","opc.iopcdigitalsignaturemanager_setsignatureoriginpartname"]
old-location: opc\iopcdigitalsignaturemanager_setsignatureoriginpartname.htm
tech.root: OPC
ms.assetid: edf1590c-14a2-4887-a2df-20b5b4cb89a6
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],SetSignatureOriginPartName method, IOpcDigitalSignatureManager.SetSignatureOriginPartName, IOpcDigitalSignatureManager::SetSignatureOriginPartName, SetSignatureOriginPartName, SetSignatureOriginPartName method [Open Packaging Conventions], SetSignatureOriginPartName method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::SetSignatureOriginPartName, opc.iopcdigitalsignaturemanager_setsignatureoriginpartname
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
 - IOpcDigitalSignatureManager::SetSignatureOriginPartName
 - msopc/IOpcDigitalSignatureManager::SetSignatureOriginPartName
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
 - IOpcDigitalSignatureManager.SetSignatureOriginPartName
---

# IOpcDigitalSignatureManager::SetSignatureOriginPartName


## -description

Sets the part name of the Digital Signature Origin part to the name represented by a specified <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer.

## -parameters

### -param signatureOriginPartName [in]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the desired part name for the Digital Signature Origin part.

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
<dt><b>OPC_E_DS_SIGNATURE_ORIGIN_EXISTS</b></dt>
<dt>0x80510054</dt>
</dl>
</td>
<td width="60%">
A Digital Signature Origin part already exists in the package and cannot be renamed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DUPLICATE_PART</b></dt>
<dt>0x8051000B</dt>
</dl>
</td>
<td width="60%">
A part with the specified part name already exists in the current package.

</td>
</tr>
</table>

## -remarks

If the Digital Signature Origin part exists or if the part name that is in the <i>signatureOriginPartName</i> parameter is being used for another part, this method will fail.


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