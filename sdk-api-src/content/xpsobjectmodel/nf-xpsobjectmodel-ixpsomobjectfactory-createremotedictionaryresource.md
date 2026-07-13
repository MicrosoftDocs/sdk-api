---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateRemoteDictionaryResource
title: IXpsOMObjectFactory::CreateRemoteDictionaryResource (xpsobjectmodel.h)
description: Creates an IXpsOMRemoteDictionaryResource interface that enables the sharing of property resources.
helpviewer_keywords: ["CreateRemoteDictionaryResource","CreateRemoteDictionaryResource method [XPS Documents and Packaging]","CreateRemoteDictionaryResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateRemoteDictionaryResource method","IXpsOMObjectFactory.CreateRemoteDictionaryResource","IXpsOMObjectFactory::CreateRemoteDictionaryResource","xps.ixpsomobjectfactory_createremotedictionaryresource","xpsobjectmodel/IXpsOMObjectFactory::CreateRemoteDictionaryResource"]
old-location: xps\ixpsomobjectfactory_createremotedictionaryresource.htm
tech.root: xps
ms.assetid: 3f3f10f0-803a-49e2-bb62-ac4124cb375a
ms.date: 12/05/2018
ms.keywords: CreateRemoteDictionaryResource, CreateRemoteDictionaryResource method [XPS Documents and Packaging], CreateRemoteDictionaryResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateRemoteDictionaryResource method, IXpsOMObjectFactory.CreateRemoteDictionaryResource, IXpsOMObjectFactory::CreateRemoteDictionaryResource, xps.ixpsomobjectfactory_createremotedictionaryresource, xpsobjectmodel/IXpsOMObjectFactory::CreateRemoteDictionaryResource
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
 - IXpsOMObjectFactory::CreateRemoteDictionaryResource
 - xpsobjectmodel/IXpsOMObjectFactory::CreateRemoteDictionaryResource
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
 - IXpsOMObjectFactory.CreateRemoteDictionaryResource
---

# IXpsOMObjectFactory::CreateRemoteDictionaryResource


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface that enables the sharing of property resources.

## -parameters

### -param dictionary [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface pointer of the dictionary to be associated with this resource.

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource.

### -param remoteDictionaryResource [out, retval]

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
<i>dictionary</i>,  <i>partUri</i>, or <i>remoteDictionaryResource</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>dictionary</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>