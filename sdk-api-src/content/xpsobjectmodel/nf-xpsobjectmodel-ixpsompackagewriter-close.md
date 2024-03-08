---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.Close
title: IXpsOMPackageWriter::Close (xpsobjectmodel.h)
description: Closes any open parts of the package, then closes the package.
helpviewer_keywords: ["Close","Close method [XPS Documents and Packaging]","Close method [XPS Documents and Packaging]","IXpsOMPackageWriter interface","Close method [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface","IXpsOMPackageWriter interface [XPS Documents and Packaging]","Close method","IXpsOMPackageWriter.Close","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","Close method","IXpsOMPackageWriter3D::Close","IXpsOMPackageWriter::Close","xps.ixpsompackagewriter_close","xpsobjectmodel/IXpsOMPackageWriter3D::Close","xpsobjectmodel/IXpsOMPackageWriter::Close"]
old-location: xps\ixpsompackagewriter_close.htm
tech.root: xps
ms.assetid: 916fbdaa-bef7-4a6f-9259-47347b47dc27
ms.date: 12/05/2018
ms.keywords: Close, Close method [XPS Documents and Packaging], Close method [XPS Documents and Packaging],IXpsOMPackageWriter interface, Close method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, IXpsOMPackageWriter interface [XPS Documents and Packaging],Close method, IXpsOMPackageWriter.Close, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],Close method, IXpsOMPackageWriter3D::Close, IXpsOMPackageWriter::Close, xps.ixpsompackagewriter_close, xpsobjectmodel/IXpsOMPackageWriter3D::Close, xpsobjectmodel/IXpsOMPackageWriter::Close
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
 - IXpsOMPackageWriter::Close
 - xpsobjectmodel/IXpsOMPackageWriter::Close
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
 - IXpsOMPackageWriter.Close
 - IXpsOMPackageWriter3D.Close
---

# IXpsOMPackageWriter::Close

## -description

Closes any open parts of the package, then closes the package.



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

If any discardable parts that are referenced by a call to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage">AddPage</a> have not been received, an error will be returned.

After this method is called, calling any other <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> method except  <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-isclosed">IsClosed</a> will return an error.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/dd464658(v=vs.85)">Using the IXpsOMPackageWriter Interface</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
