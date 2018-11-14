---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0001
title: "__MIDL___MIDL_itf_msopc_0000_0002_0001"
author: windows-sdk-content
description: Indicates the target mode of a relationship.
old-location: opc\opc_uri_target_mode.htm
tech.root: OPC
ms.assetid: af052aa3-db7a-47de-938c-32895b8735e9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OPC_URI_TARGET_MODE, OPC_URI_TARGET_MODE enumeration [Open Packaging Conventions], OPC_URI_TARGET_MODE_EXTERNAL, OPC_URI_TARGET_MODE_INTERNAL, __MIDL___MIDL_itf_msopc_0000_0002_0001, msopc/OPC_URI_TARGET_MODE, msopc/OPC_URI_TARGET_MODE_EXTERNAL, msopc/OPC_URI_TARGET_MODE_INTERNAL, opc.opc_uri_target_mode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: Opcbase.idl
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
 - OPC_URI_TARGET_MODE
product: Windows
targetos: Windows
req.typenames: OPC_URI_TARGET_MODE
req.redist: 
---

# __MIDL___MIDL_itf_msopc_0000_0002_0001 enumeration


## -description


Indicates the target mode of a relationship.


## -enum-fields




### -field OPC_URI_TARGET_MODE_INTERNAL

The target of the relationship  is a part inside the package.


### -field OPC_URI_TARGET_MODE_EXTERNAL

The target of the relationship is a resource outside of the package.


## -remarks



If the relationship's  target mode is <b>OPC_URI_TARGET_MODE_INTERNAL</b> the URI of the target  part is relative to the URI of the source of the relationship.

To get the URI of the target of the relationship, call the <a href="https://msdn.microsoft.com/65b04931-dc4e-4eb5-b542-a7b46c3164de">IOpcRelationship::GetTargetUri</a> method.

For more information about relationships, see the <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a>



<a href="https://msdn.microsoft.com/0cbf7446-d94e-447f-a82b-3d56a8036c19">IOpcRelationshipSet::CreateRelationship</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/c84246dd-f34b-40ea-8530-f93483445533">Packaging Enumerations</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>
 

 

