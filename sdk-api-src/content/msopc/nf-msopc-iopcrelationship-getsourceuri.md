---
UID: NF:msopc.IOpcRelationship.GetSourceUri
title: IOpcRelationship::GetSourceUri (msopc.h)
description: Gets the URI of the relationship source.
helpviewer_keywords: ["GetSourceUri","GetSourceUri method [Open Packaging Conventions]","GetSourceUri method [Open Packaging Conventions]","IOpcRelationship interface","IOpcRelationship interface [Open Packaging Conventions]","GetSourceUri method","IOpcRelationship.GetSourceUri","IOpcRelationship::GetSourceUri","msopc/IOpcRelationship::GetSourceUri","opc.iopcrelationship_getsourceuri"]
old-location: opc\iopcrelationship_getsourceuri.htm
tech.root: OPC
ms.assetid: 8e2587af-fce0-437a-9608-6824e861d699
ms.date: 12/05/2018
ms.keywords: GetSourceUri, GetSourceUri method [Open Packaging Conventions], GetSourceUri method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetSourceUri method, IOpcRelationship.GetSourceUri, IOpcRelationship::GetSourceUri, msopc/IOpcRelationship::GetSourceUri, opc.iopcrelationship_getsourceuri
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
 - IOpcRelationship::GetSourceUri
 - msopc/IOpcRelationship::GetSourceUri
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
 - IOpcRelationship.GetSourceUri
---

# IOpcRelationship::GetSourceUri


## -description

Gets the URI of the relationship source.

## -parameters

### -param sourceUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a> interface of the OPC URI object that represents the URI of the relationship source.

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
The <i>sourceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If the source of a relationship is the package itself, the URI in <i>sourceUri</i> represents the package root: "/".

If the relationship  target is a part, form the part name by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcuri-combineparturi">IOpcUri::CombinePartUri</a> method from the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a> interface pointer received in <i>sourceUri</i>. Use the relative URI received in the <i>targetUri</i> parameter of the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-gettargeturi">GetTargetUri</a> method as the input parameter of the <b>IOpcUri::CombinePartUri</b> call. For an example, see <a href="/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>.

For more information about relationships, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>



<a href="/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>