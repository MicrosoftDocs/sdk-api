---
UID: NF:xpsobjectmodel.IXpsOMPageReference.GetStoryFragmentsResource
title: IXpsOMPageReference::GetStoryFragmentsResource (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMStoryFragmentsResource interface of the StoryFragments part resource that is associated with the page.
helpviewer_keywords: ["GetStoryFragmentsResource","GetStoryFragmentsResource method [XPS Documents and Packaging]","GetStoryFragmentsResource method [XPS Documents and Packaging]","IXpsOMPageReference interface","IXpsOMPageReference interface [XPS Documents and Packaging]","GetStoryFragmentsResource method","IXpsOMPageReference.GetStoryFragmentsResource","IXpsOMPageReference::GetStoryFragmentsResource","xps.ixpsompagereference_getstoryfragmentsresource","xpsobjectmodel/IXpsOMPageReference::GetStoryFragmentsResource"]
old-location: xps\ixpsompagereference_getstoryfragmentsresource.htm
tech.root: xps
ms.assetid: 9b768734-07e3-4917-adb9-29989e7e2b32
ms.date: 12/05/2018
ms.keywords: GetStoryFragmentsResource, GetStoryFragmentsResource method [XPS Documents and Packaging], GetStoryFragmentsResource method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],GetStoryFragmentsResource method, IXpsOMPageReference.GetStoryFragmentsResource, IXpsOMPageReference::GetStoryFragmentsResource, xps.ixpsompagereference_getstoryfragmentsresource, xpsobjectmodel/IXpsOMPageReference::GetStoryFragmentsResource
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
 - IXpsOMPageReference::GetStoryFragmentsResource
 - xpsobjectmodel/IXpsOMPageReference::GetStoryFragmentsResource
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
 - IXpsOMPageReference.GetStoryFragmentsResource
---

# IXpsOMPageReference::GetStoryFragmentsResource


## -description

Gets a pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface of the StoryFragments part resource that is associated with the page.

## -parameters

### -param storyFragmentsResource [out, retval]

A pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface of the StoryFragments part resource that is associated with the page.  If there is no StoryFragments part, a <b>NULL</b> pointer is returned.

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
<i>storyFragmentsResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

After the resource is parsed and  loaded into the XPS OM, this method might return an error that applies to another resource. This occurs because when a resource is loaded, all of the relationships are parsed.

The StoryFragments part of a page contains the XML markup that describes the portions of one or more stories  that are associated with a single fixed page. Some of the document contents that might be described by the XML markup in a StoryFragments part include  the story's tables and paragraphs that are found on the page.

The XML markup in  the DocumentStructure and StoryFragments parts is described in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>