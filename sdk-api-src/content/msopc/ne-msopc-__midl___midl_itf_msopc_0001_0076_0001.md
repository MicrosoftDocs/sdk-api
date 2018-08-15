---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0001
title: "__MIDL___MIDL_itf_msopc_0001_0076_0001"
author: windows-sdk-content
description: Describes the canonicalization method to be applied to XML markup.
old-location: opc\opc_canonicalization_method.htm
old-project: OPC
ms.assetid: f8401d12-da2e-4b35-b473-ebe3d1f91abd
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: OPC_CANONICALIZATION_C14N, OPC_CANONICALIZATION_C14N_WITH_COMMENTS, OPC_CANONICALIZATION_METHOD, OPC_CANONICALIZATION_METHOD enumeration [Open Packaging Conventions], OPC_CANONICALIZATION_NONE, __MIDL___MIDL_itf_msopc_0001_0076_0001, msopc/OPC_CANONICALIZATION_C14N, msopc/OPC_CANONICALIZATION_C14N_WITH_COMMENTS, msopc/OPC_CANONICALIZATION_METHOD, msopc/OPC_CANONICALIZATION_NONE, opc.opc_canonicalization_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msopc.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OPC_CANONICALIZATION_METHOD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_CANONICALIZATION_METHOD
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_msopc_0001_0076_0001 enumeration


## -description


Describes the canonicalization method  to be applied to XML markup.


## -enum-fields




### -field OPC_CANONICALIZATION_NONE

No canonicalization method is applied.


### -field OPC_CANONICALIZATION_C14N

The C14N canonicalization method that removes comments is applied.


### -field OPC_CANONICALIZATION_C14N_WITH_COMMENTS

The C14N canonicalization method that preserves comments is applied.


## -remarks



For more information about XML canonicalization, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=125240">W3C Recommendation, Canonical XML
Version 1.0</a> (http://go.microsoft.com/fwlink/p/?linkid=125240).

For more information about canonicalization and packages, see the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/59c89909-6e35-4210-b76c-c820a9bb0d8e">IOpcDigitalSignature::GetCanonicalizationMethod</a>



<a href="https://msdn.microsoft.com/74cf5d3b-a350-4574-972d-1907562aece5">IOpcSignaturePartReference::GetTransformMethod</a>



<a href="https://msdn.microsoft.com/63162b37-0262-4d92-a14f-726fe4c87cc1">IOpcSignaturePartReferenceSet::Create</a>



<a href="https://msdn.microsoft.com/f3f3f6a8-c15e-420a-b56d-5dac0a054fac">IOpcSignatureReference::GetTransformMethod</a>



<a href="https://msdn.microsoft.com/5e943769-a043-4354-80e7-d471a1dbde7a">IOpcSignatureReferenceSet::Create</a>



<a href="https://msdn.microsoft.com/87d85f7e-abf2-4f6f-91b6-36a014cc0f33">IOpcSignatureRelationshipReference::GetTransformMethod</a>



<a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">IOpcSignatureRelationshipReferenceSet::Create</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/c84246dd-f34b-40ea-8530-f93483445533">Packaging Enumerations</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>



<a href="http://go.microsoft.com/fwlink/p/?linkid=125240">W3C Recommendation, Canonical XML
Version 1.0</a>
 

 

