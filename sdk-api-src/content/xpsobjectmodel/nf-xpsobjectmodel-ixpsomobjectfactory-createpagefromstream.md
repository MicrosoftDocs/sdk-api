---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePageFromStream
title: IXpsOMObjectFactory::CreatePageFromStream (xpsobjectmodel.h)
description: Reads the page markup from the specified stream to create and populate an IXpsOMPage interface.
helpviewer_keywords: ["CreatePageFromStream","CreatePageFromStream method [XPS Documents and Packaging]","CreatePageFromStream method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","FALSE","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePageFromStream method","IXpsOMObjectFactory.CreatePageFromStream","IXpsOMObjectFactory::CreatePageFromStream","TRUE","xps.ixpsomobjectfactory_createpagefromstream","xpsobjectmodel/IXpsOMObjectFactory::CreatePageFromStream"]
old-location: xps\ixpsomobjectfactory_createpagefromstream.htm
tech.root: xps
ms.assetid: daeafc73-33b0-4c88-b92d-da4ca42b19a9
ms.date: 12/05/2018
ms.keywords: CreatePageFromStream, CreatePageFromStream method [XPS Documents and Packaging], CreatePageFromStream method [XPS Documents and Packaging],IXpsOMObjectFactory interface, FALSE, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePageFromStream method, IXpsOMObjectFactory.CreatePageFromStream, IXpsOMObjectFactory::CreatePageFromStream, TRUE, xps.ixpsomobjectfactory_createpagefromstream, xpsobjectmodel/IXpsOMObjectFactory::CreatePageFromStream
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
 - IXpsOMObjectFactory::CreatePageFromStream
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePageFromStream
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
 - IXpsOMObjectFactory.CreatePageFromStream
---

# IXpsOMObjectFactory::CreatePageFromStream


## -description

Reads the page markup from the specified stream to create and populate an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface.

## -parameters

### -param pageMarkupStream [in]

The stream that contains the page markup.

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the page's URI.

### -param resources [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a> interface that contains the resources used by the page.

### -param reuseObjects [in]

A Boolean value that specifies  whether  the software  is to attempt to optimize the page contents tree by sharing objects that are identical in all properties and children. 

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

### -param page [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface created by this method.

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
<i>pageMarkupStream</i>, <i>partUri</i>, <i>resources</i>, or   <i>page</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>resources</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

This method does not validate the contents of any stream-based resources that it loads from the stream  into the document objects. The application must verify these resources before it uses them.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>