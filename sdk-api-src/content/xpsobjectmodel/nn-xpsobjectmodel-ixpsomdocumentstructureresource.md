---
UID: NN:xpsobjectmodel.IXpsOMDocumentStructureResource
title: IXpsOMDocumentStructureResource
author: windows-sdk-content
description: Provides access to the XML content of the resource stream of the DocumentStructure part.
old-location: xps\ixpsomdocumentstructureresource.htm
tech.root: printdocs
ms.assetid: a0cc8748-08b2-4471-9961-603786e983a4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMDocumentStructureResource, IXpsOMDocumentStructureResource interface [XPS Documents and Packaging], IXpsOMDocumentStructureResource interface [XPS Documents and Packaging],described, xps.ixpsomdocumentstructureresource, xpsobjectmodel/IXpsOMDocumentStructureResource
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMDocumentStructureResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDocumentStructureResource interface


## -description


Provides access to the  XML content of the resource stream of the DocumentStructure part.The <b>IXpsOMDocumentStructureResource</b> interface enables a program to read  and replace the XML content of the DocumentStructure part.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMDocumentStructureResource</b> interface inherits from <a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>. <b>IXpsOMDocumentStructureResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMDocumentStructureResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbaedef0-f1a9-4c2c-88ae-1542cfbff252">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface that contains the resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77c08ced-bc0d-4ebf-a257-d4298c7a352d">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b58e0ca-03e7-43ea-aab2-5ac6cdb15807">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be associated with this resource.

</td>
</tr>
</table> 


## -remarks



The <i>DocumentStructure</i> part of an XPS document contains the document outline, which, along with the <i>StoryFragments</i> parts, defines the reading order of every element that appears in the fixed pages of the document. 

The reading order of an XPS document is organized into semantic blocks called stories. Stories are logical units of the document, in the same way that  articles are units in a magazine. Stories are made up of one or more StoryFragments parts; <i>StoryFragments</i> parts contain the XML markup that defines the story's semantic blocks, which describe the structure of the document's content. Examples of a story's semantic blocks include  paragraphs and tables.

The XML markup  in the DocumentStructure and StoryFragments parts is described in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.




## -see-also




<a href="https://msdn.microsoft.com/ce41c5fb-033d-4140-b7aa-4f28676f0ae6">IXpsOMObjectFactory::CreateDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>



<a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

