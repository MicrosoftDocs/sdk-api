---
UID: NF:xpsobjectmodel.IXpsOMPackage.GetDiscardControlPartName
title: IXpsOMPackage::GetDiscardControlPartName (xpsobjectmodel.h)
description: Gets the name of the discard control part in the XPS package.
helpviewer_keywords: ["GetDiscardControlPartName","GetDiscardControlPartName method [XPS Documents and Packaging]","GetDiscardControlPartName method [XPS Documents and Packaging]","IXpsOMPackage interface","IXpsOMPackage interface [XPS Documents and Packaging]","GetDiscardControlPartName method","IXpsOMPackage.GetDiscardControlPartName","IXpsOMPackage::GetDiscardControlPartName","xps.ixpsompackage_getdiscardcontrolpartname","xpsobjectmodel/IXpsOMPackage::GetDiscardControlPartName"]
old-location: xps\ixpsompackage_getdiscardcontrolpartname.htm
tech.root: xps
ms.assetid: e1c60001-0a0c-4ff9-bb17-fef3e47b16a6
ms.date: 12/05/2018
ms.keywords: GetDiscardControlPartName, GetDiscardControlPartName method [XPS Documents and Packaging], GetDiscardControlPartName method [XPS Documents and Packaging],IXpsOMPackage interface, IXpsOMPackage interface [XPS Documents and Packaging],GetDiscardControlPartName method, IXpsOMPackage.GetDiscardControlPartName, IXpsOMPackage::GetDiscardControlPartName, xps.ixpsompackage_getdiscardcontrolpartname, xpsobjectmodel/IXpsOMPackage::GetDiscardControlPartName
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
 - IXpsOMPackage::GetDiscardControlPartName
 - xpsobjectmodel/IXpsOMPackage::GetDiscardControlPartName
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
 - IXpsOMPackage.GetDiscardControlPartName
---

# IXpsOMPackage::GetDiscardControlPartName


## -description

Gets the name of the discard control part in the XPS package.

## -parameters

### -param discardControlPartUri [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the name of the discard control part in the XPS package. If a discard control part has not been set, a <b>NULL</b> pointer is returned.

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
<i>discardControlPartUri</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>