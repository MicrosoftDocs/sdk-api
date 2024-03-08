---
UID: NF:msopc.IOpcPackage.GetPartSet
title: IOpcPackage::GetPartSet (msopc.h)
description: Gets a part set object that contains IOpcPart interface pointers.
helpviewer_keywords: ["GetPartSet","GetPartSet method [Open Packaging Conventions]","GetPartSet method [Open Packaging Conventions]","IOpcPackage interface","IOpcPackage interface [Open Packaging Conventions]","GetPartSet method","IOpcPackage.GetPartSet","IOpcPackage::GetPartSet","msopc/IOpcPackage::GetPartSet","opc.iopcpackage_getpartset"]
old-location: opc\iopcpackage_getpartset.htm
tech.root: OPC
ms.assetid: 9460e057-8fe8-46b8-b12e-ba761fcaf49b
ms.date: 12/05/2018
ms.keywords: GetPartSet, GetPartSet method [Open Packaging Conventions], GetPartSet method [Open Packaging Conventions],IOpcPackage interface, IOpcPackage interface [Open Packaging Conventions],GetPartSet method, IOpcPackage.GetPartSet, IOpcPackage::GetPartSet, msopc/IOpcPackage::GetPartSet, opc.iopcpackage_getpartset
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
 - IOpcPackage::GetPartSet
 - msopc/IOpcPackage::GetPartSet
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
 - IOpcPackage.GetPartSet
---

# IOpcPackage::GetPartSet


## -description

Gets a part set object that contains <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface pointers.

## -parameters

### -param partSet [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a> interface of the part set object that contains <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface pointers to part objects.

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
The <i>partSet</i> parameter is <b>NULL</b>.

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

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface is only used to represent parts in the package that are not Relationships parts.

For more information about packages, parts, relationships, and the interfaces that represent them, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory">IOpcFactory</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage">IOpcPackage</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packages-overview">Packages Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>