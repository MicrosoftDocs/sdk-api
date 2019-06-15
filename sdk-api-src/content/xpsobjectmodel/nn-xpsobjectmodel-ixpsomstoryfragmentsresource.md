---
UID: NN:xpsobjectmodel.IXpsOMStoryFragmentsResource
title: IXpsOMStoryFragmentsResource (xpsobjectmodel.h)
author: windows-sdk-content
description: Provides access to the content of the resource stream of a page's StoryFragments part.
old-location: xps\ixpsomstoryfragmentsresource.htm
tech.root: printdocs
ms.assetid: 83bc8017-c679-40a8-96a8-bff9aa2273af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMStoryFragmentsResource, IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging], IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging],described, xps.ixpsomstoryfragmentsresource, xpsobjectmodel/IXpsOMStoryFragmentsResource
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMStoryFragmentsResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMStoryFragmentsResource interface


## -description


Provides access to the content of the resource stream of a page's StoryFragments part.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMStoryFragmentsResource</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMStoryFragmentsResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMStoryFragmentsResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomstoryfragmentsresource-getowner">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface that contains this resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomstoryfragmentsresource-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomstoryfragmentsresource-setcontent">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be associated with this resource.

</td>
</tr>
</table> 


## -remarks



The StoryFragments part of a page contains the XML markup that describes the   portions of one or more stories  that are associated with a single fixed page. Some of the document contents that might be described by the XML markup in a StoryFragments part include  the story's tables and paragraphs that are found on the page.

The XML markup  of the DocumentStructure and StoryFragments parts is described in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createstoryfragmentsresource">IXpsOMObjectFactory::CreateStoryFragmentsResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

