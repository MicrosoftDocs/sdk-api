---
UID: NF:msopc.IOpcRelationship.GetTargetMode
title: IOpcRelationship::GetTargetMode (msopc.h)
description: Gets a value that describes whether the relationship's target is internal or external to the package.
helpviewer_keywords: ["GetTargetMode","GetTargetMode method [Open Packaging Conventions]","GetTargetMode method [Open Packaging Conventions]","IOpcRelationship interface","IOpcRelationship interface [Open Packaging Conventions]","GetTargetMode method","IOpcRelationship.GetTargetMode","IOpcRelationship::GetTargetMode","msopc/IOpcRelationship::GetTargetMode","opc.iopcrelationship_gettargetmode"]
old-location: opc\iopcrelationship_gettargetmode.htm
tech.root: OPC
ms.assetid: 5fb103c9-cb73-46b3-9102-6811d6673faf
ms.date: 12/05/2018
ms.keywords: GetTargetMode, GetTargetMode method [Open Packaging Conventions], GetTargetMode method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetTargetMode method, IOpcRelationship.GetTargetMode, IOpcRelationship::GetTargetMode, msopc/IOpcRelationship::GetTargetMode, opc.iopcrelationship_gettargetmode
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
 - IOpcRelationship::GetTargetMode
 - msopc/IOpcRelationship::GetTargetMode
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
 - IOpcRelationship.GetTargetMode
---

# IOpcRelationship::GetTargetMode


## -description

Gets a value that describes whether the relationship's target is internal  or external to the package.

## -parameters

### -param targetMode [out, retval]

A value  that describes whether the relationship's target is internal or external to the package.

If the target of the relationship is internal, the target is a part.

If the target of the relationship is external, the target is a resource outside of the package.

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
The <i>targetMode</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If the relationship target is internal, the  target is a part. The URI of the target is relative to the URI of the source part.

To get the URI of the target of the relationship, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-gettargeturi">IOpcRelationship::GetTargetUri</a> method.

The definitive way to find a part of interest is by using a relationship type.

Finding a part of interest requires several steps. For detailed information about finding a part, see the <a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a> and  <a href="/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>.

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



<a href="/windows/win32/api/msopc/ne-msopc-opc_uri_target_mode">OPC_URI_TARGET_MODE</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>