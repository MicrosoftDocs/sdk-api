---
UID: NF:msopc.IOpcRelationship.GetId
title: IOpcRelationship::GetId (msopc.h)
description: Gets the unique identifier of the relationship.
helpviewer_keywords: ["GetId","GetId method [Open Packaging Conventions]","GetId method [Open Packaging Conventions]","IOpcRelationship interface","IOpcRelationship interface [Open Packaging Conventions]","GetId method","IOpcRelationship.GetId","IOpcRelationship::GetId","msopc/IOpcRelationship::GetId","opc.iopcrelationship_getid"]
old-location: opc\iopcrelationship_getid.htm
tech.root: OPC
ms.assetid: 8646d592-d568-4b82-80f3-2673cd0d2721
ms.date: 12/05/2018
ms.keywords: GetId, GetId method [Open Packaging Conventions], GetId method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetId method, IOpcRelationship.GetId, IOpcRelationship::GetId, msopc/IOpcRelationship::GetId, opc.iopcrelationship_getid
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
 - IOpcRelationship::GetId
 - msopc/IOpcRelationship::GetId
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
 - IOpcRelationship.GetId
---

# IOpcRelationship::GetId


## -description

Gets the unique identifier of the relationship.

## -parameters

### -param relationshipIdentifier [out, retval]

The identifier of the relationship.

The identifier of a relationship is arbitrary and local to the package, and, therefore, .

Valid identifiers conform to the restrictions for <b>xsd:ID</b>, which are  documented in section 3.3.8 ID of the <a href="https://www.w3.org/TR/xmlschema-2/#ID">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a> (http://www.w3.org/TR/xmlschema-2/#ID).

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
The <i>relationshipIdentifier</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The identifier of a relationship is not useful for finding relationships because it is arbitrary and local to the package.

The definitive way to find a part of interest is by using a relationship type.

Finding a part requires several steps. For detailed information about finding a part, see <a href="/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>.

This method allocates memory used by the string returned in <i>relationshipIdentifier</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

For more information about relationships, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>



<a href="https://www.w3.org/TR/xmlschema-2/#ID">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a>