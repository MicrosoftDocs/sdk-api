---
UID: NF:msopc.IOpcPart.GetName
title: IOpcPart::GetName (msopc.h)
description: Gets a part URI object that represents the part name.
helpviewer_keywords: ["GetName","GetName method [Open Packaging Conventions]","GetName method [Open Packaging Conventions]","IOpcPart interface","IOpcPart interface [Open Packaging Conventions]","GetName method","IOpcPart.GetName","IOpcPart::GetName","msopc/IOpcPart::GetName","opc.iopcpart_getname"]
old-location: opc\iopcpart_getname.htm
tech.root: OPC
ms.assetid: 83fed005-c061-4f1d-8b2b-73397e0b7a92
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Open Packaging Conventions], GetName method [Open Packaging Conventions],IOpcPart interface, IOpcPart interface [Open Packaging Conventions],GetName method, IOpcPart.GetName, IOpcPart::GetName, msopc/IOpcPart::GetName, opc.iopcpart_getname
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
 - IOpcPart::GetName
 - msopc/IOpcPart::GetName
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
 - IOpcPart.GetName
---

# IOpcPart::GetName


## -description

Gets a part URI object that represents the part name.

## -parameters

### -param name [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of the part URI object that represents the part name.

Part names conform to specific syntax specified in the <i>OPC</i>.

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
The <i>name</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For more information about parts, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>OPC</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>