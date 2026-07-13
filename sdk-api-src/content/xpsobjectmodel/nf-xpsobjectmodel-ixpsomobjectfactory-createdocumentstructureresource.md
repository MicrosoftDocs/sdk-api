---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateDocumentStructureResource
title: IXpsOMObjectFactory::CreateDocumentStructureResource (xpsobjectmodel.h)
description: Creates an IXpsOMDocumentStructureResource interface, which provides access to the document structure resource stream.
helpviewer_keywords: ["CreateDocumentStructureResource","CreateDocumentStructureResource method [XPS Documents and Packaging]","CreateDocumentStructureResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateDocumentStructureResource method","IXpsOMObjectFactory.CreateDocumentStructureResource","IXpsOMObjectFactory::CreateDocumentStructureResource","xps.ixpsomobjectfactory_createdocumentstructureresource","xpsobjectmodel/IXpsOMObjectFactory::CreateDocumentStructureResource"]
old-location: xps\ixpsomobjectfactory_createdocumentstructureresource.htm
tech.root: xps
ms.assetid: ce41c5fb-033d-4140-b7aa-4f28676f0ae6
ms.date: 12/05/2018
ms.keywords: CreateDocumentStructureResource, CreateDocumentStructureResource method [XPS Documents and Packaging], CreateDocumentStructureResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateDocumentStructureResource method, IXpsOMObjectFactory.CreateDocumentStructureResource, IXpsOMObjectFactory::CreateDocumentStructureResource, xps.ixpsomobjectfactory_createdocumentstructureresource, xpsobjectmodel/IXpsOMObjectFactory::CreateDocumentStructureResource
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
 - IXpsOMObjectFactory::CreateDocumentStructureResource
 - xpsobjectmodel/IXpsOMObjectFactory::CreateDocumentStructureResource
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
 - IXpsOMObjectFactory.CreateDocumentStructureResource
---

# IXpsOMObjectFactory::CreateDocumentStructureResource


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface, which provides access to the document structure resource stream.

## -parameters

### -param acquiredStream [in]

The read-only <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>   interface to be associated with this resource. This parameter must not be <b>NULL</b>.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource. This parameter must not be <b>NULL</b>.

### -param documentStructureResource [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface.

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
<i>acquiredStream</i>,  <i>partUri</i>, or <i>documentStructureResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The DocumentStructure part of an XPS document contains the document outline, which, with the StoryFragments parts, defines the reading order of every element that appears in the fixed pages of the document. This interface enables a program to read the XML contents of the DocumentStructure  part and also to replace the XML contents of the DocumentStructure part.

The DocumentStructure part contains the document framework and the outline that describes the overall reading order of the document. The reading order is organized into semantic blocks called stories. Stories are logical units of the document in the same way as  articles are units in a magazine. Stories are made up of one or more StoryFragments parts.

The  StoryFragments parts contain content structure markup that defines the story's semantic blocks, such as the  paragraphs and tables that make up the story's content.

The content of the DocumentStructure and StoryFragments parts is described in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>