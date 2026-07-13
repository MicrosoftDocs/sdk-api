---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.IsClosed
title: IXpsOMPackageWriter::IsClosed (xpsobjectmodel.h)
description: Gets the status of the IXpsOMPackageWriter interface.
helpviewer_keywords: ["FALSE","IXpsOMPackageWriter interface [XPS Documents and Packaging]","IsClosed method","IXpsOMPackageWriter.IsClosed","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","IsClosed method","IXpsOMPackageWriter3D::IsClosed","IXpsOMPackageWriter::IsClosed","IsClosed","IsClosed method [XPS Documents and Packaging]","IsClosed method [XPS Documents and Packaging]","IXpsOMPackageWriter interface","IsClosed method [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface","TRUE","xps.ixpsompackagewriter_isclosed","xpsobjectmodel/IXpsOMPackageWriter3D::IsClosed","xpsobjectmodel/IXpsOMPackageWriter::IsClosed"]
old-location: xps\ixpsompackagewriter_isclosed.htm
tech.root: xps
ms.assetid: 7f782432-3d36-466c-b265-9da99d97565e
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMPackageWriter interface [XPS Documents and Packaging],IsClosed method, IXpsOMPackageWriter.IsClosed, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],IsClosed method, IXpsOMPackageWriter3D::IsClosed, IXpsOMPackageWriter::IsClosed, IsClosed, IsClosed method [XPS Documents and Packaging], IsClosed method [XPS Documents and Packaging],IXpsOMPackageWriter interface, IsClosed method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, TRUE, xps.ixpsompackagewriter_isclosed, xpsobjectmodel/IXpsOMPackageWriter3D::IsClosed, xpsobjectmodel/IXpsOMPackageWriter::IsClosed
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
 - IXpsOMPackageWriter::IsClosed
 - xpsobjectmodel/IXpsOMPackageWriter::IsClosed
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
 - IXpsOMPackageWriter.IsClosed
 - IXpsOMPackageWriter3D.IsClosed
---

# IXpsOMPackageWriter::IsClosed


## -description

Gets the status of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface.

## -parameters

### -param isClosed [out, retval]

A pointer to a Boolean variable that receives the status of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The package is closed and no more content can be added.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The  package is open and content can be added.

</td>
</tr>
</table>

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
<dt><b>XPS_E_UNAVAILABLE_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
A severe error occurred and the contents of the XPS OM might be unrecoverable. Some components of the XPS OM might still be usable but only after they have been verified. Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

If the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface is closed,  operations on the package are not allowed.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/dd464658(v=vs.85)">Using the IXpsOMPackageWriter Interface</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>