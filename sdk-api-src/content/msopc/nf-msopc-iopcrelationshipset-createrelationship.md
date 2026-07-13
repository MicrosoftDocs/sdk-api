---
UID: NF:msopc.IOpcRelationshipSet.CreateRelationship
title: IOpcRelationshipSet::CreateRelationship (msopc.h)
description: Creates a relationship object that represents a specified relationship, then adds to the set a pointer to the object's IOpcRelationship interface.
helpviewer_keywords: ["CreateRelationship","CreateRelationship method [Open Packaging Conventions]","CreateRelationship method [Open Packaging Conventions]","IOpcRelationshipSet interface","IOpcRelationshipSet interface [Open Packaging Conventions]","CreateRelationship method","IOpcRelationshipSet.CreateRelationship","IOpcRelationshipSet::CreateRelationship","msopc/IOpcRelationshipSet::CreateRelationship","opc.iopcrelationshipset_createrelationship"]
old-location: opc\iopcrelationshipset_createrelationship.htm
tech.root: OPC
ms.assetid: 0cbf7446-d94e-447f-a82b-3d56a8036c19
ms.date: 12/05/2018
ms.keywords: CreateRelationship, CreateRelationship method [Open Packaging Conventions], CreateRelationship method [Open Packaging Conventions],IOpcRelationshipSet interface, IOpcRelationshipSet interface [Open Packaging Conventions],CreateRelationship method, IOpcRelationshipSet.CreateRelationship, IOpcRelationshipSet::CreateRelationship, msopc/IOpcRelationshipSet::CreateRelationship, opc.iopcrelationshipset_createrelationship
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
 - IOpcRelationshipSet::CreateRelationship
 - msopc/IOpcRelationshipSet::CreateRelationship
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
 - IOpcRelationshipSet.CreateRelationship
---

# IOpcRelationshipSet::CreateRelationship


## -description

Creates a relationship object that represents a specified relationship, then adds to  the set a pointer to the object's <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface.

## -parameters

### -param relationshipIdentifier [in]

A unique identifier of the relationship to be represented as the relationship object. To use a randomly generated identifier, pass <b>NULL</b> to this parameter.

Valid identifiers conform to the restrictions for <b>xsd:ID</b>, which are  documented in section 3.3.8 ID of the <a href="https://www.w3.org/TR/xmlschema-2/#ID">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a> (http://www.w3.org/TR/xmlschema-2/#ID).

### -param relationshipType [in]

The relationship type that defines the role of  the relationship to be represented as the relationship object.

### -param targetUri [in]

A  URI to the target of the relationship to be represented as the relationship object.

If the value in <i>targetMode</i> is <b>OPC_URI_TARGET_MODE_INTERNAL</b>, target is a part and the URI must be relative to the source of the relationship.

If the value in <i>targetMode</i> is <b>OPC_URI_TARGET_MODE_EXTERNAL</b>, target is a resource outside of the package and the URI may be absolute or relative to the location of the package.

For more information about the URI of a relationship's target, see the <i>OPC</i>.

### -param targetMode [in]

A value that indicates whether the target of the relationship to be represented as the relationship object is internal or external to  the package.

### -param relationship [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface  of the relationship object that represents the relationship. 

This parameter can be <b>NULL</b> if a pointer to the  new object is not needed.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>targetMode</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_uri_target_mode">OPC_URI_TARGET_MODE</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the <i>relationshipType</i> and <i>targetUri</i> parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DUPLICATE_RELATIONSHIP</b></dt>
<dt>0x80510013</dt>
</dl>
</td>
<td width="60%">
A relationship with the same identifier already exists in the current package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_INVALID_RELATIONSHIP_ID</b></dt>
<dt>0x80510010</dt>
</dl>
</td>
<td width="60%">
The <b>Id</b> attribute of a relationship does not conform to the rules specified in the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_INVALID_RELATIONSHIP_TARGET</b></dt>
<dt>0x80510012</dt>
</dl>
</td>
<td width="60%">
The URI in <i>targetUri</i> is absolute and the value in <i>targetMode</i> is <b>OPC_URI_TARGET_MODE_INTERNAL</b>. The target's URI must be relative when this target mode is specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_INVALID_RELATIONSHIP_TARGET</b></dt>
<dt>0x80510012</dt>
</dl>
</td>
<td width="60%">
The <b>Target</b> attribute of a relationship does not conform to the rules specified in the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_INVALID_RELATIONSHIP_TYPE</b></dt>
<dt>0x80510011</dt>
</dl>
</td>
<td width="60%">
The <b>Type</b> attribute of a relationship does not conform to the rules specified in the <i>OPC</i>.

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

When a relationship object is created and a pointer to it is added to the set, the relationship it represents is saved when the package is saved.

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface provides access to relationship properties. For details about these properties, see the <a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a> and <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_uri_target_mode">OPC_URI_TARGET_MODE</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>



<a href="https://www.w3.org/TR/xmlschema-2/#ID">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a>