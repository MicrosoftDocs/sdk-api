---
UID: NF:msopc.IOpcSignatureRelationshipReference.GetRelationshipSigningOption
title: IOpcSignatureRelationshipReference::GetRelationshipSigningOption (msopc.h)
author: windows-sdk-content
description: Gets a value that describes whether all or a subset of relationships that are stored in the referenced&#160;Relationships part are selected.
old-location: opc\iopcsignaturerelationshipreference_getrelationshipsigningoption.htm
tech.root: OPC
ms.assetid: 9960c67c-4f09-435e-b82c-ca449645f6e5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRelationshipSigningOption, GetRelationshipSigningOption method [Open Packaging Conventions], GetRelationshipSigningOption method [Open Packaging Conventions],IOpcSignatureRelationshipReference interface, IOpcSignatureRelationshipReference interface [Open Packaging Conventions],GetRelationshipSigningOption method, IOpcSignatureRelationshipReference.GetRelationshipSigningOption, IOpcSignatureRelationshipReference::GetRelationshipSigningOption, msopc/IOpcSignatureRelationshipReference::GetRelationshipSigningOption, opc.iopcsignaturerelationshipreference_getrelationshipsigningoption
ms.topic: method
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
 - IOpcSignatureRelationshipReference.GetRelationshipSigningOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcSignatureRelationshipReference::GetRelationshipSigningOption


## -description


Gets a value that describes whether all or a subset of relationships that are stored in the referenced Relationships part are selected.


## -parameters




### -param relationshipSigningOption [out, retval]

A value that describes whether all or a subset of relationships are selected.


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
The <i>relationshipSigningOption</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/ne-msopc-__midl___midl_itf_msopc_0001_0076_0003">OPC_RELATIONSHIPS_SIGNING_OPTION</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

