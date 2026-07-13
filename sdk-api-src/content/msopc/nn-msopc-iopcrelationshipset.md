---
UID: NN:msopc.IOpcRelationshipSet
title: IOpcRelationshipSet (msopc.h)
description: Represents a Relationships part as an unordered set of IOpcRelationship interface pointers to relationship objects.
helpviewer_keywords: ["IOpcRelationshipSet","IOpcRelationshipSet interface [Open Packaging Conventions]","IOpcRelationshipSet interface [Open Packaging Conventions]","described","msopc/IOpcRelationshipSet","opc.iopcrelationshipset"]
old-location: opc\iopcrelationshipset.htm
tech.root: OPC
ms.assetid: 6259906d-820d-4b6e-bbeb-d9d044f2b35a
ms.date: 12/05/2018
ms.keywords: IOpcRelationshipSet, IOpcRelationshipSet interface [Open Packaging Conventions], IOpcRelationshipSet interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSet, opc.iopcrelationshipset
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
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
 - IOpcRelationshipSet
 - msopc/IOpcRelationshipSet
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
 - IOpcRelationshipSet
---

# IOpcRelationshipSet interface


## -description

Represents a Relationships part as an unordered set of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers to relationship objects.

## -inheritance

The <b>IOpcRelationshipSet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcRelationshipSet</b> also has these types of members:

## -remarks

When a relationship object is created and a pointer to it is added to the set, the relationship it represents is saved when the package is saved.

When an  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer is deleted from the set, the relationship it represents is not saved when the package is saved.

If a relationship is represented in the set, the relationship is stored in the Relationships part represented as the set.

For how to form the part name for the target of a relationship, see <a href="/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>.

For more information about relationships, see <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface provides access to relationship properties. For details about these properties, see the <a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a> and <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipenumerator">IOpcRelationshipEnumerator</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>
