---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0003
title: "__MIDL___MIDL_itf_msopc_0001_0076_0003"
author: windows-sdk-content
description: Describes whether a reference represented by the IOpcSignatureRelationshipReference interface refers to all or a subset of relationships represented as relationship objects in a relationship set object.
old-location: opc\opc_relationships_signing_option.htm
tech.root: OPC
ms.assetid: b6a83730-459a-4119-a013-7d670e659c32
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OPC_RELATIONSHIPS_SIGNING_OPTION, OPC_RELATIONSHIPS_SIGNING_OPTION enumeration [Open Packaging Conventions], OPC_RELATIONSHIP_SIGN_PART, OPC_RELATIONSHIP_SIGN_USING_SELECTORS, __MIDL___MIDL_itf_msopc_0001_0076_0003, msopc/OPC_RELATIONSHIPS_SIGNING_OPTION, msopc/OPC_RELATIONSHIP_SIGN_PART, msopc/OPC_RELATIONSHIP_SIGN_USING_SELECTORS, opc.opc_relationships_signing_option
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msopc.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_RELATIONSHIPS_SIGNING_OPTION
product: Windows
targetos: Windows
req.typenames: OPC_RELATIONSHIPS_SIGNING_OPTION
req.redist: 
---

# __MIDL___MIDL_itf_msopc_0001_0076_0003 enumeration


## -description


Describes whether a reference represented by the <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface refers to all or a subset of relationships represented as relationship objects in a relationship set object.


## -enum-fields




### -field OPC_RELATIONSHIP_SIGN_USING_SELECTORS

The reference refers to a subset of relationships represented as relationship objects and identified using the <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface.


### -field OPC_RELATIONSHIP_SIGN_PART

The reference refers to all of the relationships represented as relationship objects in the relationship set object.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/9960c67c-4f09-435e-b82c-ca449645f6e5">IOpcSignatureRelationshipReference::GetRelationshipSigningOption</a>



<a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">IOpcSignatureRelationshipReferenceSet::Create</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/c84246dd-f34b-40ea-8530-f93483445533">Packaging Enumerations</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

