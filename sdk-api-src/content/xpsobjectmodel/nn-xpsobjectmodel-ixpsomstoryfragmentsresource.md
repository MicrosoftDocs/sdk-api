---
UID: NN:xpsobjectmodel.IXpsOMStoryFragmentsResource
title: IXpsOMStoryFragmentsResource (xpsobjectmodel.h)
description: Provides access to the content of the resource stream of a page's StoryFragments part.
helpviewer_keywords: ["IXpsOMStoryFragmentsResource","IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging]","IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging]","described","xps.ixpsomstoryfragmentsresource","xpsobjectmodel/IXpsOMStoryFragmentsResource"]
old-location: xps\ixpsomstoryfragmentsresource.htm
tech.root: xps
ms.assetid: 83bc8017-c679-40a8-96a8-bff9aa2273af
ms.date: 12/05/2018
ms.keywords: IXpsOMStoryFragmentsResource, IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging], IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging],described, xps.ixpsomstoryfragmentsresource, xpsobjectmodel/IXpsOMStoryFragmentsResource
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
 - IXpsOMStoryFragmentsResource
 - xpsobjectmodel/IXpsOMStoryFragmentsResource
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
 - IXpsOMStoryFragmentsResource
---

# IXpsOMStoryFragmentsResource interface

## -description

Provides access to the content of the resource stream of a page's StoryFragments part.

## -inheritance

The <b>IXpsOMStoryFragmentsResource</b> interface inherits from <a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMStoryFragmentsResource</b> also has these types of members:

## -remarks

The StoryFragments part of a page contains the XML markup that describes the   portions of one or more stories  that are associated with a single fixed page. Some of the document contents that might be described by the XML markup in a StoryFragments part include  the story's tables and paragraphs that are found on the page.

The XML markup  of the DocumentStructure and StoryFragments parts is described in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createstoryfragmentsresource">IXpsOMObjectFactory::CreateStoryFragmentsResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
