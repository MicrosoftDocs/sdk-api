---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIAutomationTextRange3::GetChildrenBuildCache


## -description


Returns the children and supplied properties and patterns for elements in a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/714e9d91-c6b9-4fa2-8a14-9bdd721b3135">GetChildren</a>, but adds the standard build cache pattern.


## -parameters




### -param cacheRequest [in]

An <a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a> specifying the properties and control patterns to be cached.


### -param children [out, retval]

Returns the children, and each child’s properties or patterns, of the text range that meet the criteria of the supplied <i>cacheRequest</i>.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -remarks



	Following the design of <a href="https://msdn.microsoft.com/714e9d91-c6b9-4fa2-8a14-9bdd721b3135">GetChildren</a>:

<ul>
<li>Children that overlap with the text range, but are not entirely enclosed by it will also be included.</li>
<li>When no children exist, an empty collection is returned.</li>
</ul>
As a result of a successful call, UI Automation clients are able call "Cached" APIs of <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> that are provided in the <i>cacheRequest</i>, for example, <a href="https://msdn.microsoft.com/3cd093fe-04ee-4b09-b5e7-28dad984951e">IUIAutomationElement::GetCachedPropertyValue</a>.




## -see-also




<a href="https://msdn.microsoft.com/3491996E-89EF-496D-94B6-FF8D121D3828">IUIAutomationTextRange3</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

