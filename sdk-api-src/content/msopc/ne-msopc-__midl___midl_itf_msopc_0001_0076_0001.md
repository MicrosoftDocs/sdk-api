---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

