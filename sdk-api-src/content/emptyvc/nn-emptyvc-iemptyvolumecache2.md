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

# IEmptyVolumeCache2 interface


## -description


Extends <a href="https://msdn.microsoft.com/ba3797c2-f82c-4721-b72d-8552683a10d2">IEmptyVolumeCache</a>. This interface defines one additional method, <a href="https://msdn.microsoft.com/42f39dcd-0292-4121-89e9-80145b1c1c7d">InitializeEx</a>, that provides better localization support than <a href="https://msdn.microsoft.com/e0d66c58-6963-4694-984f-6f4a710d08c0">IEmptyVolumeCache::Initialize</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEmptyVolumeCache2</b> interface inherits from <a href="https://msdn.microsoft.com/ba3797c2-f82c-4721-b72d-8552683a10d2">IEmptyVolumeCache</a>. <b>IEmptyVolumeCache2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEmptyVolumeCache2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f39dcd-0292-4121-89e9-80145b1c1c7d">InitializeEx</a>
</td>
<td align="left" width="63%">
Initializes the disk cleanup handler. It provides better support for localization than <a href="https://msdn.microsoft.com/e0d66c58-6963-4694-984f-6f4a710d08c0">IEmptyVolumeCache::Initialize</a>.

</td>
</tr>
</table> 


## -remarks



This interface should be exported by disk cleanup handlers running on Windows 2000. Handlers running on Windows 98 must export <a href="https://msdn.microsoft.com/ba3797c2-f82c-4721-b72d-8552683a10d2">IEmptyVolumeCache</a>.




## -see-also




<a href="https://msdn.microsoft.com/ba3797c2-f82c-4721-b72d-8552683a10d2">IEmptyVolumeCache</a>



<a href="https://msdn.microsoft.com/d6775458-3b39-4ee8-90f9-d8a749bd1800">IEmptyVolumeCacheCallBack</a>
 

 

