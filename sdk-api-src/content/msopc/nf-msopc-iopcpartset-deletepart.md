---
UID: NF:msopc.IOpcPartSet.DeletePart
title: IOpcPartSet::DeletePart (msopc.h)
description: Deletes the IOpcPart interface pointer of a specified part object from the set.
helpviewer_keywords: ["DeletePart","DeletePart method [Open Packaging Conventions]","DeletePart method [Open Packaging Conventions]","IOpcPartSet interface","IOpcPartSet interface [Open Packaging Conventions]","DeletePart method","IOpcPartSet.DeletePart","IOpcPartSet::DeletePart","msopc/IOpcPartSet::DeletePart","opc.iopcpartset_deletepart"]
old-location: opc\iopcpartset_deletepart.htm
tech.root: OPC
ms.assetid: 2d69530f-7e10-409a-8832-f410d6f9582e
ms.date: 12/05/2018
ms.keywords: DeletePart, DeletePart method [Open Packaging Conventions], DeletePart method [Open Packaging Conventions],IOpcPartSet interface, IOpcPartSet interface [Open Packaging Conventions],DeletePart method, IOpcPartSet.DeletePart, IOpcPartSet::DeletePart, msopc/IOpcPartSet::DeletePart, opc.iopcpartset_deletepart
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
 - IOpcPartSet::DeletePart
 - msopc/IOpcPartSet::DeletePart
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
 - IOpcPartSet.DeletePart
---

# IOpcPartSet::DeletePart


## -description

Deletes the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface pointer of a specified part object from the set.

## -parameters

### -param name [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object that represents the part name.

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

When an  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface pointer is deleted from the set, the part it represents is not serialized when the package is serialized. Additionally, if the represented part is the source of one or more relationships, those relationships are not saved with the package when the package object is written.

The data contained in a deleted part object is accessible until the package object that contains the deleted part object is released. Additionally, a Relationship whose source is the part that is represented by the deleted part object also remains accessible until the package object that contains the deleted part object is released. However, these relationships will not be saved when the package is saved.


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



<b>Reference</b>