---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePackageFromStream
title: IXpsOMObjectFactory::CreatePackageFromStream (xpsobjectmodel.h)
description: Opens a stream that contains an XPS package, and returns an instantiated XPS document object tree.
helpviewer_keywords: ["CreatePackageFromStream","CreatePackageFromStream method [XPS Documents and Packaging]","CreatePackageFromStream method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","FALSE","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePackageFromStream method","IXpsOMObjectFactory.CreatePackageFromStream","IXpsOMObjectFactory::CreatePackageFromStream","TRUE","xps.ixpsomobjectfactory_createpackagefromstream","xpsobjectmodel/IXpsOMObjectFactory::CreatePackageFromStream"]
old-location: xps\ixpsomobjectfactory_createpackagefromstream.htm
tech.root: xps
ms.assetid: 4a4bb128-9480-4e50-8848-a2e1e715f4e3
ms.date: 12/05/2018
ms.keywords: CreatePackageFromStream, CreatePackageFromStream method [XPS Documents and Packaging], CreatePackageFromStream method [XPS Documents and Packaging],IXpsOMObjectFactory interface, FALSE, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePackageFromStream method, IXpsOMObjectFactory.CreatePackageFromStream, IXpsOMObjectFactory::CreatePackageFromStream, TRUE, xps.ixpsomobjectfactory_createpackagefromstream, xpsobjectmodel/IXpsOMObjectFactory::CreatePackageFromStream
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
 - IXpsOMObjectFactory::CreatePackageFromStream
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePackageFromStream
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
 - IXpsOMObjectFactory.CreatePackageFromStream
---

# IXpsOMObjectFactory::CreatePackageFromStream


## -description

Opens a stream that contains an XPS package, and returns an instantiated XPS document object  tree.

## -parameters

### -param stream [in]

The stream that contains an XPS package.

### -param reuseObjects [in]

The  Boolean value that indicates   that the software  is to attempt to optimize the document object tree by sharing objects that are identical in all properties and children. 

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
The software will attempt to optimize the object tree.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The software will not attempt to optimize the object tree.

</td>
</tr>
</table>

### -param package [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a> interface that contains the resulting XPS document object tree.

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
<i>stream</i>  or   <i>package</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

This method does not validate the contents of any stream-based resources that it loads from the stream  into the  objects of the XPS OM. Instead, the application must validate these resources before it uses them.

This method does not deserialize the document pages; it only deserializes the XPS package down to the page reference parts. The actual pages can be deserialized as they are needed, by calling the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage">IXpsOMPageReference::GetPage</a> method. Because the pages are not deserialized when   <b>GetPage</b>  is called, it is possible for this method to return S_OK or, if an attempt is made to load a problematic page  in an XPS package, to return an error.

If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.

Some of the changes that can occur in such a case are listed in the table that follows:<table>
<tr>
<th>Document feature</th>
<th>Action</th>
</tr>
<tr>
<td>
Digital signatures

</td>
<td>
Removed from document

</td>
</tr>
<tr>
<td>
DiscardControl part

</td>
<td>
Removed from document

</td>
</tr>
<tr>
<td>
Foreign document parts

</td>
<td>
Removed from document

</td>
</tr>
<tr>
<td>
FixedPage markup

</td>
<td>
Modified from original

</td>
</tr>
<tr>
<td>
Resource dictionary markup

</td>
<td>
Modified from original if Optimization flag is set

</td>
</tr>
</table>
 



For information about using <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a> interface in a program, see <a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>