---
UID: NF:xpsobjectmodel.IXpsOMPageReference.SetStoryFragmentsResource
title: IXpsOMPageReference::SetStoryFragmentsResource (xpsobjectmodel.h)
description: Sets the IXpsOMStoryFragmentsResource interface pointer of the StoryFragments resource to be assigned to the page.
helpviewer_keywords: ["IXpsOMPageReference interface [XPS Documents and Packaging]","SetStoryFragmentsResource method","IXpsOMPageReference.SetStoryFragmentsResource","IXpsOMPageReference::SetStoryFragmentsResource","SetStoryFragmentsResource","SetStoryFragmentsResource method [XPS Documents and Packaging]","SetStoryFragmentsResource method [XPS Documents and Packaging]","IXpsOMPageReference interface","xps.ixpsompagereference_setstoryfragmentsresource","xpsobjectmodel/IXpsOMPageReference::SetStoryFragmentsResource"]
old-location: xps\ixpsompagereference_setstoryfragmentsresource.htm
tech.root: xps
ms.assetid: 0e096e8f-d2f1-4dcb-9a86-c56ff53393d1
ms.date: 12/05/2018
ms.keywords: IXpsOMPageReference interface [XPS Documents and Packaging],SetStoryFragmentsResource method, IXpsOMPageReference.SetStoryFragmentsResource, IXpsOMPageReference::SetStoryFragmentsResource, SetStoryFragmentsResource, SetStoryFragmentsResource method [XPS Documents and Packaging], SetStoryFragmentsResource method [XPS Documents and Packaging],IXpsOMPageReference interface, xps.ixpsompagereference_setstoryfragmentsresource, xpsobjectmodel/IXpsOMPageReference::SetStoryFragmentsResource
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
 - IXpsOMPageReference::SetStoryFragmentsResource
 - xpsobjectmodel/IXpsOMPageReference::SetStoryFragmentsResource
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
 - IXpsOMPageReference.SetStoryFragmentsResource
---

# IXpsOMPageReference::SetStoryFragmentsResource


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface pointer of the StoryFragments resource to be assigned to the page.

## -parameters

### -param storyFragmentsResource [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface of the StoryFragments part resource to be assigned to the page. If an <b>IXpsOMStoryFragmentsResource</b> interface has been set, a <b>NULL</b> pointer will release it.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>storyFragmentsResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

The StoryFragments part of a page contains the XML markup that describes  the portions of one or more stories  that are associated with a single fixed page. Some of the document contents that might be described by the XML markup in a StoryFragments part include  the story's tables and paragraphs that are found on the page.

The XML markup  of the DocumentStructure and StoryFragments parts is described in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>