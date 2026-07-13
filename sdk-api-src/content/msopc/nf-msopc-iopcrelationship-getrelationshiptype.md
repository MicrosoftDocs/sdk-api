---
UID: NF:msopc.IOpcRelationship.GetRelationshipType
title: IOpcRelationship::GetRelationshipType (msopc.h)
description: Gets the relationship type.
helpviewer_keywords: ["GetRelationshipType","GetRelationshipType method [Open Packaging Conventions]","GetRelationshipType method [Open Packaging Conventions]","IOpcRelationship interface","IOpcRelationship interface [Open Packaging Conventions]","GetRelationshipType method","IOpcRelationship.GetRelationshipType","IOpcRelationship::GetRelationshipType","msopc/IOpcRelationship::GetRelationshipType","opc.iopcrelationship_getrelationshiptype"]
old-location: opc\iopcrelationship_getrelationshiptype.htm
tech.root: OPC
ms.assetid: da832c8e-99e1-452a-90eb-97580f00f003
ms.date: 12/05/2018
ms.keywords: GetRelationshipType, GetRelationshipType method [Open Packaging Conventions], GetRelationshipType method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetRelationshipType method, IOpcRelationship.GetRelationshipType, IOpcRelationship::GetRelationshipType, msopc/IOpcRelationship::GetRelationshipType, opc.iopcrelationship_getrelationshiptype
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
 - IOpcRelationship::GetRelationshipType
 - msopc/IOpcRelationship::GetRelationshipType
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
 - IOpcRelationship.GetRelationshipType
---

# IOpcRelationship::GetRelationshipType


## -description

Gets the relationship type.

## -parameters

### -param relationshipType [out, retval]

Receives the relationship type, which is the qualified name of the relationship, as defined by the package format designer or the <i>OPC</i>.

For more information about relationship types see Remarks.

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
The <i>relationshipType</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>relationshipType</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

The definitive way to find a part of interest is by using a relationship type.

Finding a part of interest requires several steps. For detailed information about finding a part, see <a href="/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>.

For more information about relationships, relationship types and a list of relationship types defined by the OPC, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>OPC</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getenumeratorfortype">IOpcRelationshipSet::GetEnumeratorForType</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>