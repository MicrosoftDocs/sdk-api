---
UID: NN:xpsobjectmodel.IXpsOMDocumentStructureResource
title: IXpsOMDocumentStructureResource (xpsobjectmodel.h)
description: Provides access to the XML content of the resource stream of the DocumentStructure part.
helpviewer_keywords: ["IXpsOMDocumentStructureResource","IXpsOMDocumentStructureResource interface [XPS Documents and Packaging]","IXpsOMDocumentStructureResource interface [XPS Documents and Packaging]","described","xps.ixpsomdocumentstructureresource","xpsobjectmodel/IXpsOMDocumentStructureResource"]
old-location: xps\ixpsomdocumentstructureresource.htm
tech.root: xps
ms.assetid: a0cc8748-08b2-4471-9961-603786e983a4
ms.date: 12/05/2018
ms.keywords: IXpsOMDocumentStructureResource, IXpsOMDocumentStructureResource interface [XPS Documents and Packaging], IXpsOMDocumentStructureResource interface [XPS Documents and Packaging],described, xps.ixpsomdocumentstructureresource, xpsobjectmodel/IXpsOMDocumentStructureResource
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
 - IXpsOMDocumentStructureResource
 - xpsobjectmodel/IXpsOMDocumentStructureResource
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
 - IXpsOMDocumentStructureResource
---

# IXpsOMDocumentStructureResource interface

## -description

Provides access to the  XML content of the resource stream of the DocumentStructure part.The <b>IXpsOMDocumentStructureResource</b> interface enables a program to read  and replace the XML content of the DocumentStructure part.

## -inheritance

The <b>IXpsOMDocumentStructureResource</b> interface inherits from <a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMDocumentStructureResource</b> also has these types of members:

## -remarks

The <i>DocumentStructure</i> part of an XPS document contains the document outline, which, along with the <i>StoryFragments</i> parts, defines the reading order of every element that appears in the fixed pages of the document. 

The reading order of an XPS document is organized into semantic blocks called stories. Stories are logical units of the document, in the same way that  articles are units in a magazine. Stories are made up of one or more StoryFragments parts; <i>StoryFragments</i> parts contain the XML markup that defines the story's semantic blocks, which describe the structure of the document's content. Examples of a story's semantic blocks include  paragraphs and tables.

The XML markup  in the DocumentStructure and StoryFragments parts is described in the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createdocumentstructureresource">IXpsOMObjectFactory::CreateDocumentStructureResource</a>



<a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
