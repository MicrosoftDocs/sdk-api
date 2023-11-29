---
UID: NF:msopc.IOpcPackage.GetRelationshipSet
title: IOpcPackage::GetRelationshipSet (msopc.h)
description: Gets a relationship set object that represents the Relationships part that stores package relationships.
helpviewer_keywords: ["GetRelationshipSet","GetRelationshipSet method [Open Packaging Conventions]","GetRelationshipSet method [Open Packaging Conventions]","IOpcPackage interface","IOpcPackage interface [Open Packaging Conventions]","GetRelationshipSet method","IOpcPackage.GetRelationshipSet","IOpcPackage::GetRelationshipSet","msopc/IOpcPackage::GetRelationshipSet","opc.iopcpackage_getrelationshipset"]
old-location: opc\iopcpackage_getrelationshipset.htm
tech.root: OPC
ms.assetid: 316fe21c-675a-47ec-b17e-0fe505a06c7f
ms.date: 12/05/2018
ms.keywords: GetRelationshipSet, GetRelationshipSet method [Open Packaging Conventions], GetRelationshipSet method [Open Packaging Conventions],IOpcPackage interface, IOpcPackage interface [Open Packaging Conventions],GetRelationshipSet method, IOpcPackage.GetRelationshipSet, IOpcPackage::GetRelationshipSet, msopc/IOpcPackage::GetRelationshipSet, opc.iopcpackage_getrelationshipset
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcobjectmodel.idl
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
 - IOpcPackage::GetRelationshipSet
 - msopc/IOpcPackage::GetRelationshipSet
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
 - IOpcPackage.GetRelationshipSet
---

# IOpcPackage::GetRelationshipSet


## -description

Gets a relationship set object that represents the Relationships part that stores package relationships.

## -parameters

### -param relationshipSet [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a> interface of the relationship set object. The set represents the Relationships part that stores package relationships.

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
The <i>relationshipSet</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Package Consumption error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/package-consumption-error-group">Package Consumption Error Group</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Part URI error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/part-uri-error-group">Part URI Error Group</a>. 

</td>
</tr>
</table>

## -remarks

The Package relationships represented in the set provide the entry point to a package for an application.

For more information about packages, parts, relationships, and the interfaces that represent them, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage">IOpcPackage</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packages-overview">Packages Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>