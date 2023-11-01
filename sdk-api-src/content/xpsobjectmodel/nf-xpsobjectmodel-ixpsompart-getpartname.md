---
UID: NF:xpsobjectmodel.IXpsOMPart.GetPartName
title: IXpsOMPart::GetPartName (xpsobjectmodel.h)
description: Gets the name that will be used when the part is serialized.
helpviewer_keywords: ["GetPartName","GetPartName method [XPS Documents and Packaging]","GetPartName method [XPS Documents and Packaging]","IXpsOMPart interface","IXpsOMPart interface [XPS Documents and Packaging]","GetPartName method","IXpsOMPart.GetPartName","IXpsOMPart::GetPartName","xps.ixpsompart_getpartname","xpsobjectmodel/IXpsOMPart::GetPartName"]
old-location: xps\ixpsompart_getpartname.htm
tech.root: xps
ms.assetid: 43793c60-5fa3-4895-8a6a-7e010e65ac3e
ms.date: 12/05/2018
ms.keywords: GetPartName, GetPartName method [XPS Documents and Packaging], GetPartName method [XPS Documents and Packaging],IXpsOMPart interface, IXpsOMPart interface [XPS Documents and Packaging],GetPartName method, IXpsOMPart.GetPartName, IXpsOMPart::GetPartName, xps.ixpsompart_getpartname, xpsobjectmodel/IXpsOMPart::GetPartName
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - IXpsOMPart::GetPartName
 - xpsobjectmodel/IXpsOMPart::GetPartName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPart.GetPartName
---

# IXpsOMPart::GetPartName


## -description

Gets the name that will be used when the part is serialized.

## -parameters

### -param partUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name. If the part name has not been set (by the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompart-setpartname">SetPartName</a> method), a <b>NULL</b> pointer is returned.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>partUri</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>