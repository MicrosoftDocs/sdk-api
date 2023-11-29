---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateRemoteDictionaryResourceFromStream
title: IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream (xpsobjectmodel.h)
description: Loads the remote resource dictionary markup into an unrooted IXpsOMRemoteDictionaryResource interface.
helpviewer_keywords: ["CreateRemoteDictionaryResourceFromStream","CreateRemoteDictionaryResourceFromStream method [XPS Documents and Packaging]","CreateRemoteDictionaryResourceFromStream method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateRemoteDictionaryResourceFromStream method","IXpsOMObjectFactory.CreateRemoteDictionaryResourceFromStream","IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream","xps.ixpsomobjectfactory_createremotedictionaryresourcefromstream","xpsobjectmodel/IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream"]
old-location: xps\ixpsomobjectfactory_createremotedictionaryresourcefromstream.htm
tech.root: xps
ms.assetid: 996a97f5-320f-4e51-af15-f3b125d4f6c8
ms.date: 12/05/2018
ms.keywords: CreateRemoteDictionaryResourceFromStream, CreateRemoteDictionaryResourceFromStream method [XPS Documents and Packaging], CreateRemoteDictionaryResourceFromStream method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateRemoteDictionaryResourceFromStream method, IXpsOMObjectFactory.CreateRemoteDictionaryResourceFromStream, IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream, xps.ixpsomobjectfactory_createremotedictionaryresourcefromstream, xpsobjectmodel/IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream
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
 - IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream
 - xpsobjectmodel/IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream
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
 - IXpsOMObjectFactory.CreateRemoteDictionaryResourceFromStream
---

# IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream


## -description

Loads the  remote resource dictionary markup into an unrooted <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface.

## -parameters

### -param dictionaryMarkupStream [in]

The <b>IStream</b> interface that contains the remote resource dictionary markup.

### -param dictionaryPartUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource.

### -param resources [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a> interface for the part resources of the dictionary resource objects  that have streams.

### -param dictionaryResource [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface.

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
<i>dictionaryMarkupStream</i>,  <i>dictionaryPartUri</i>, <i>resources</i>, or <i>dictionaryResource</i> is <b>NULL</b>.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>