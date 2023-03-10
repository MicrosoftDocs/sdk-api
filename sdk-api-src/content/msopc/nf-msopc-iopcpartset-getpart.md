---
UID: NF:msopc.IOpcPartSet.GetPart
title: IOpcPartSet::GetPart (msopc.h)
description: Gets a part object, which represents a specified part, in the set.
helpviewer_keywords: ["GetPart","GetPart method [Open Packaging Conventions]","GetPart method [Open Packaging Conventions]","IOpcPartSet interface","IOpcPartSet interface [Open Packaging Conventions]","GetPart method","IOpcPartSet.GetPart","IOpcPartSet::GetPart","msopc/IOpcPartSet::GetPart","opc.iopcpartset_getpart"]
old-location: opc\iopcpartset_getpart.htm
tech.root: OPC
ms.assetid: 3a44725b-23a0-4338-b618-c0ce4ecde204
ms.date: 12/05/2018
ms.keywords: GetPart, GetPart method [Open Packaging Conventions], GetPart method [Open Packaging Conventions],IOpcPartSet interface, IOpcPartSet interface [Open Packaging Conventions],GetPart method, IOpcPartSet.GetPart, IOpcPartSet::GetPart, msopc/IOpcPartSet::GetPart, opc.iopcpartset_getpart
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
 - IOpcPartSet::GetPart
 - msopc/IOpcPartSet::GetPart
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
 - IOpcPartSet.GetPart
---

# IOpcPartSet::GetPart


## -description

Gets a part object, which represents a specified part, in the set.

## -parameters

### -param name [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object that represents the part name of a part.

### -param part [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> of the part object that represents the part that has the specified part name.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NO_SUCH_PART</b></dt>
<dt>0x80510018</dt>
</dl>
</td>
<td width="60%">
The specified part does not exist.

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

To retrieve the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface pointer of the part object that represents a specific part, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartset-partexists">PartExists</a> method and pass in the part name to confirm that the part is represented in the set. If it is, call the <b>GetPart</b> method and pass in the part name to retrieve the <b>IOpcPart</b> interface pointer.

If the part URI object represents the part name of a Relationships part, this method will fail because Relationships parts are not included in the set.

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface provides access to the properties of a part. For details about these properties, see the <a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a> and <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a>.


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