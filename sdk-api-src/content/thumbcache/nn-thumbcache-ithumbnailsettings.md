---
UID: NN:thumbcache.IThumbnailSettings
title: IThumbnailSettings
author: windows-sdk-content
description: Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request.
old-location: shell\IThumbnailSettings.htm
old-project: shell
ms.assetid: 502537E5-1D72-44f0-BC75-DBED61F174FC
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IThumbnailSettings, IThumbnailSettings interface [Windows Shell], IThumbnailSettings interface [Windows Shell],described, shell.IThumbnailSettings, thumbcache/IThumbnailSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - IThumbnailSettings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IThumbnailSettings interface


## -description


Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThumbnailSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IThumbnailSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IThumbnailSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556644">SetContext</a>
</td>
<td align="left" width="63%">
Enables a thumbnail provider to return a thumbnail specific to the user's context.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
This interface can be implemented by any thumbnail provider that supports <a href="https://msdn.microsoft.com/28a13749-89e7-407e-89cb-95464859ce3e">IExtractImage</a> or <a href="https://msdn.microsoft.com/55c4739a-4835-4f53-a435-804ddf06ffcf">IThumbnailProvider</a>.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

