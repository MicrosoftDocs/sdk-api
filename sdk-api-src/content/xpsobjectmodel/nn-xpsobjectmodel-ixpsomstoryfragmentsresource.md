---
UID: NN:xpsobjectmodel.IXpsOMStoryFragmentsResource
title: IXpsOMStoryFragmentsResource
author: windows-sdk-content
description: Provides access to the content of the resource stream of a page's StoryFragments part.
old-location: xps\ixpsomstoryfragmentsresource.htm
old-project: printdocs
ms.assetid: 83bc8017-c679-40a8-96a8-bff9aa2273af
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMStoryFragmentsResource, IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging], IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging],described, xps.ixpsomstoryfragmentsresource, xpsobjectmodel/IXpsOMStoryFragmentsResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_INTERLEAVING
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
req.lib: XpsPrint.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMStoryFragmentsResource interface


## -description


Provides access to the content of the resource stream of a page's StoryFragments part.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMStoryFragmentsResource</b> interface inherits from <a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>. <b>IXpsOMStoryFragmentsResource</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8dc44277-d296-4747-8dd7-8901a94b5213">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface that contains this resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c119f1c6-59c0-41b2-b79d-5de9a62c146a">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/861d9688-932b-4830-b52b-acd505524608">SetContent</a>
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




<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/b0e3f538-4af9-4d86-8899-6ea4e601eaad">IXpsOMObjectFactory::CreateStoryFragmentsResource</a>



<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

