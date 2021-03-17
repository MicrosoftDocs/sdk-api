---
UID: NF:msopc.IOpcPartSet.PartExists
title: IOpcPartSet::PartExists (msopc.h)
description: Gets a value that indicates whether a specified part is represented as a part object in the set.
helpviewer_keywords: ["IOpcPartSet interface [Open Packaging Conventions]","PartExists method","IOpcPartSet.PartExists","IOpcPartSet::PartExists","PartExists","PartExists method [Open Packaging Conventions]","PartExists method [Open Packaging Conventions]","IOpcPartSet interface","msopc/IOpcPartSet::PartExists","opc.iopcpartset_partexists"]
old-location: opc\iopcpartset_partexists.htm
tech.root: OPC
ms.assetid: 721e0252-330a-4218-9267-b3dd0dea7598
ms.date: 12/05/2018
ms.keywords: IOpcPartSet interface [Open Packaging Conventions],PartExists method, IOpcPartSet.PartExists, IOpcPartSet::PartExists, PartExists, PartExists method [Open Packaging Conventions], PartExists method [Open Packaging Conventions],IOpcPartSet interface, msopc/IOpcPartSet::PartExists, opc.iopcpartset_partexists
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
 - IOpcPartSet::PartExists
 - msopc/IOpcPartSet::PartExists
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
 - IOpcPartSet.PartExists
---

# IOpcPartSet::PartExists


## -description

Gets a value that indicates whether a specified part is represented as a part object in the set.

## -parameters

### -param name [in]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>  that represents the part name of the part.

### -param partExists [out, retval]

One of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
A part that has the specified part name is represented in the set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
A part that has the specified part name is not represented in the set.

</td>
</tr>
</table>

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
The <i>partExists</i> parameter is <b>NULL</b>.

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

To retrieve the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface pointer of the part object that represents a specific part, call the <b>PartExists</b> method and pass in the part name to confirm that the part is represented in the set. If it is, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartset-getpart">GetPart</a> method and pass in the part name to retrieve the <b>IOpcPart</b> interface pointer.

If the represented part name is the name of a Relationships part, <i>partExists</i> is receives <b>FALSE</b> because Relationships parts are not included in the set.

If a part is represented in the set, the part exists in the package being read or the package to be written.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>