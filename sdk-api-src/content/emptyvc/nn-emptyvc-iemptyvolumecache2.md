---
UID: NN:emptyvc.IEmptyVolumeCache2
title: IEmptyVolumeCache2
author: windows-sdk-content
description: Extends IEmptyVolumeCache. This interface defines one additional method, InitializeEx, that provides better localization support than IEmptyVolumeCache::Initialize.
old-location: lwef\iemptyvolumecache2.htm
tech.root: lwef
ms.assetid: a3e941ee-0477-48a8-96bd-c9d74c66ca41
ms.author: windowssdkdev
ms.date: 10/31/2018
ms.keywords: IEmptyVolumeCache2, IEmptyVolumeCache2 interface [Legacy Windows Environment Features], IEmptyVolumeCache2 interface [Legacy Windows Environment Features],described, _win32_IEmptyVolumeCache2, emptyvc/IEmptyVolumeCache2, lwef.iemptyvolumecache2, shell.iemptyvolumecache2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: emptyvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEmptyVolumeCache2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

