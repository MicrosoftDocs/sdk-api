---
UID: NN:emptyvc.IEmptyVolumeCache
title: IEmptyVolumeCache
author: windows-sdk-content
description: Used by the disk cleanup manager to communicate with a disk cleanup handler. Exposes methods that enable the manager to request information from a handler, and notify it of events such as the start of a scan or purge.
old-location: lwef\iemptyvolumecache.htm
old-project: lwef
ms.assetid: ba3797c2-f82c-4721-b72d-8552683a10d2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEmptyVolumeCache, IEmptyVolumeCache interface [Legacy Windows Environment Features], IEmptyVolumeCache interface [Legacy Windows Environment Features],described, _win32_IEmptyVolumeCache, emptyvc/IEmptyVolumeCache, lwef.iemptyvolumecache, shell.iemptyvolumecache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: emptyvc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EMI_VERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEmptyVolumeCache
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEmptyVolumeCache interface


## -description


Used by the disk cleanup manager to communicate with a disk cleanup handler. Exposes methods that enable the manager to request information from a handler, and notify it of events such as the start of a scan or purge.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEmptyVolumeCache</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEmptyVolumeCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEmptyVolumeCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb374e09-92f5-4efb-8e93-0ddc2975c2c1">Deactivate</a>
</td>
<td align="left" width="63%">
Notifies the handler that the disk cleanup manager is shutting down. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8ec2f70-f327-49d4-babb-a9640f105003">GetSpaceUsed</a>
</td>
<td align="left" width="63%">
Requests the amount of disk space that the disk cleanup handler can free.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0d66c58-6963-4694-984f-6f4a710d08c0">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the disk cleanup handler, based on the information stored under the specified registry key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42430da-9d6a-42e9-bc4f-325d986c7c48">Purge</a>
</td>
<td align="left" width="63%">
Notifies the handler to start deleting its unneeded files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bce6251-b209-405a-8ac2-fd385f1c69ee">ShowProperties</a>
</td>
<td align="left" width="63%">
Notifies the handler to display its UI. 

</td>
</tr>
</table> 


## -remarks



This interface must be implemented by disk cleanup handlers running on Windows 98. Handlers running on Windows 2000 should also expose <a href="https://msdn.microsoft.com/a3e941ee-0477-48a8-96bd-c9d74c66ca41">IEmptyVolumeCache2</a>.




## -see-also




<a href="https://msdn.microsoft.com/d6775458-3b39-4ee8-90f9-d8a749bd1800">IEmptyVolumeCacheCallBack</a>
 

 

