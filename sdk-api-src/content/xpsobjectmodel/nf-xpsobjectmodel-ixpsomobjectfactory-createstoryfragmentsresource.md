---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateStoryFragmentsResource
title: IXpsOMObjectFactory::CreateStoryFragmentsResource (xpsobjectmodel.h)
description: Creates an IXpsOMStoryFragmentsResource interface that provides access to the content of the resource stream of a page's StoryFragments part.
helpviewer_keywords: ["CreateStoryFragmentsResource","CreateStoryFragmentsResource method [XPS Documents and Packaging]","CreateStoryFragmentsResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateStoryFragmentsResource method","IXpsOMObjectFactory.CreateStoryFragmentsResource","IXpsOMObjectFactory::CreateStoryFragmentsResource","xps.ixpsomobjectfactory_createstoryfragmentsresource","xpsobjectmodel/IXpsOMObjectFactory::CreateStoryFragmentsResource"]
old-location: xps\ixpsomobjectfactory_createstoryfragmentsresource.htm
tech.root: xps
ms.assetid: b0e3f538-4af9-4d86-8899-6ea4e601eaad
ms.date: 12/05/2018
ms.keywords: CreateStoryFragmentsResource, CreateStoryFragmentsResource method [XPS Documents and Packaging], CreateStoryFragmentsResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateStoryFragmentsResource method, IXpsOMObjectFactory.CreateStoryFragmentsResource, IXpsOMObjectFactory::CreateStoryFragmentsResource, xps.ixpsomobjectfactory_createstoryfragmentsresource, xpsobjectmodel/IXpsOMObjectFactory::CreateStoryFragmentsResource
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
 - IXpsOMObjectFactory::CreateStoryFragmentsResource
 - xpsobjectmodel/IXpsOMObjectFactory::CreateStoryFragmentsResource
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
 - IXpsOMObjectFactory.CreateStoryFragmentsResource
---

# IXpsOMObjectFactory::CreateStoryFragmentsResource


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface that provides access to the content of the resource stream of a page's StoryFragments part.

## -parameters

### -param acquiredStream [in]

The read-only <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to be associated with this StoryFragments  resource.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to  this resource.

### -param storyFragmentsResource [out, retval]

A pointer to the new  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface.

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
<i>acquiredStream</i>,  <i>partUri</i>, or <i>storyFragmentsResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The StoryFragments part of a page contains the XML markup that describes the structure of the portions of one or more stories  that are associated with a single fixed page. Some of the document contents that might be described by the XML markup in a StoryFragments part include  the story's tables and paragraphs that are found on the page.

The XML markup in  the DocumentStructure and StoryFragments parts is described in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>