---
UID: NN:oleidl.IOleContainer
title: IOleContainer
author: windows-sdk-content
description: Enumerates objects in a compound document or lock a container in the running state. Container and object applications both implement this interface.
old-location: com\iolecontainer.htm
tech.root: com
ms.assetid: 98549309-8ac8-4391-92ab-8a62269ff579
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOleContainer, IOleContainer interface [COM], IOleContainer interface [COM],described, _ole_iolecontainer, com.iolecontainer, oleidl/IOleContainer
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IOleContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleContainer interface


## -description


Enumerates objects in a compound document or lock a container in the running state. Container and object applications both implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleContainer</b> interface inherits from <a href="https://msdn.microsoft.com/37844d9b-35ce-4d30-8a58-dac4c671896f">IParseDisplayName</a>. <b>IOleContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d825c71-506c-4fd3-ab48-6006f2858d05">EnumObjects</a>
</td>
<td align="left" width="63%">
Enumerates the objects in the current container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31b9961a-29a2-48bf-9d39-d86718983682">LockContainer</a>
</td>
<td align="left" width="63%">
Keeps the container for embedded objects running until explicitly released.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a>



<a href="https://msdn.microsoft.com/37844d9b-35ce-4d30-8a58-dac4c671896f">IParseDisplayName</a>
 

 

