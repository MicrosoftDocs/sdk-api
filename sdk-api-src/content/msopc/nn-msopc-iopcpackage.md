---
UID: NN:msopc.IOpcPackage
title: IOpcPackage (msopc.h)
description: Represents a package and provides methods to access the package's parts and relationships.
helpviewer_keywords: ["IOpcPackage","IOpcPackage interface [Open Packaging Conventions]","IOpcPackage interface [Open Packaging Conventions]","described","msopc/IOpcPackage","opc.iopcpackage"]
old-location: opc\iopcpackage.htm
tech.root: OPC
ms.assetid: e7052dd2-c910-41d8-a58a-8f3e68e09dd0
ms.date: 12/05/2018
ms.keywords: IOpcPackage, IOpcPackage interface [Open Packaging Conventions], IOpcPackage interface [Open Packaging Conventions],described, msopc/IOpcPackage, opc.iopcpackage
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
 - IOpcPackage
 - msopc/IOpcPackage
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
 - IOpcPackage
---

# IOpcPackage interface


## -description

Represents a package and provides methods to access the package's parts and relationships.

## -inheritance

The <b>IOpcPackage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcPackage</b> also has these types of members:

## -remarks

To get a pointer to this interface, call either the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createpackage">IOpcFactory::CreatePackage</a> or <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-readpackagefromstream">IOpcFactory::ReadPackageFromStream</a> method.

Package relationships serve as an entry point  to the package by  links from the package to target  resources. The target of a package relationship is often an important part described in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i> or by the package format designer.

For example, a package relationship can provide access to the Core Properties part that stores package metadata, or to a part containing format-specific data, where the part and data are described by the package designer.  The Main Document part of the word processing OpenXML format is one such format-specific part. For more information about this part, see Part 1: Fundamentals in <a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a> (https://www.ecma-international.org/publications-and-standards/standards/ecma-376/).

The definitive way to find a part of interest is by using a relationship type. Several steps are required; for details, see the <a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a> and the <a href="/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a> how-to task.

For more information about packages, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>OPC</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packages-overview">Packages Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>
