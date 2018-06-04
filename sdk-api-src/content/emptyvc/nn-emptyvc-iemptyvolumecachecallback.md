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

# IEmptyVolumeCacheCallBack interface


## -description


Exposes methods that are used by a disk cleanup handler to communicate with the disk cleanup manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEmptyVolumeCacheCallBack</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEmptyVolumeCacheCallBack</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEmptyVolumeCacheCallBack</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96b97919-9b3b-418e-a76a-a2e8aad453b9">PurgeProgress</a>
</td>
<td align="left" width="63%">
Called periodically by a disk cleanup handler to update the disk cleanup manager on the progress of a purge of deletable files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41ebc9db-d402-47d7-b303-f87357ae820d">ScanProgress</a>
</td>
<td align="left" width="63%">
Called by a disk cleanup handler to update the disk cleanup manager on the progress of a scan for deletable files.

</td>
</tr>
</table> 


## -remarks



A disk cleanup handler uses this interface to report to the disk cleanup manager on the progress either of deleting files or of scanning for deletable files. It also provides a way to query the manager, to find out if the user has canceled the operation. The handler receives a pointer to this interface when the manager calls the <a href="https://msdn.microsoft.com/c8ec2f70-f327-49d4-babb-a9640f105003">IEmptyVolumeCache::GetSpaceUsed</a> or <a href="https://msdn.microsoft.com/c42430da-9d6a-42e9-bc4f-325d986c7c48">IEmptyVolumeCache::Purge</a> methods.



