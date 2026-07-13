---
UID: NF:msopc.IOpcRelationship.GetTargetUri
title: IOpcRelationship::GetTargetUri (msopc.h)
description: Gets the URI of the relationship target.
helpviewer_keywords: ["GetTargetUri","GetTargetUri method [Open Packaging Conventions]","GetTargetUri method [Open Packaging Conventions]","IOpcRelationship interface","IOpcRelationship interface [Open Packaging Conventions]","GetTargetUri method","IOpcRelationship.GetTargetUri","IOpcRelationship::GetTargetUri","msopc/IOpcRelationship::GetTargetUri","opc.iopcrelationship_gettargeturi"]
old-location: opc\iopcrelationship_gettargeturi.htm
tech.root: OPC
ms.assetid: 65b04931-dc4e-4eb5-b542-a7b46c3164de
ms.date: 12/05/2018
ms.keywords: GetTargetUri, GetTargetUri method [Open Packaging Conventions], GetTargetUri method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetTargetUri method, IOpcRelationship.GetTargetUri, IOpcRelationship::GetTargetUri, msopc/IOpcRelationship::GetTargetUri, opc.iopcrelationship_gettargeturi
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
 - IOpcRelationship::GetTargetUri
 - msopc/IOpcRelationship::GetTargetUri
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
 - IOpcRelationship.GetTargetUri
---

# IOpcRelationship::GetTargetUri


## -description

Gets the URI of the relationship target.

## -parameters

### -param targetUri [out, retval]

A pointer to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a> interface of the URI that represents the URI of the relationship's target.

If the relationship target is internal, the  target is a part and the URI of the target is relative to the URI of the source part.

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
The <i>targetUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The definitive way to find a part of interest is by using a relationship type.

Finding a part of interest requires several steps. For detailed information about finding a part, see the <a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a> and <a href="/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>.

To determine whether the target of the relationship is internal or external, call the <b>GetTargetUri</b> method.

If the relationship target is internal, the target is a part.

If the relationship target is a part, the URI in <i>targetUri</i> is relative to the URI of the relationship source.

If the relationship  target is a part, form the part name by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcuri-combineparturi">IOpcUri::CombinePartUri</a> method from the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcuri">IOpcUri</a> interface pointer received in <i>sourceUri</i> parameter of the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getsourceuri">GetSourceUri</a> method. Use the relative URI received in <i>targetUri</i> as the input parameter of the <b>IOpcUri::CombinePartUri</b> call. For an example, see <a href="/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>.

For more information about relationships, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_uri_target_mode">OPC_URI_TARGET_MODE</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>



<a href="/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>