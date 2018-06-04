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

# ISynchronizeContainer interface


## -description


Manages a group of unsignaled synchronization objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronizeContainer</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ISynchronizeContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronizeContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2d48de3-848c-4cc9-bd96-fffbb2ca2ba3">AddSynchronize</a>
</td>
<td align="left" width="63%">
Adds a synchronization object to the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2754b744-3ba8-4e60-9847-1d0eb3c24180">WaitMultiple</a>
</td>
<td align="left" width="63%">
Waits for any synchronization object in the container to be signaled or for a specified timeout period to elapse, whichever comes first.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6">ISynchronize</a>
 

 

