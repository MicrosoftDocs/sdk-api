---
UID: NN:emptyvc.IEmptyVolumeCacheCallBack
title: IEmptyVolumeCacheCallBack
author: windows-sdk-content
description: Exposes methods that are used by a disk cleanup handler to communicate with the disk cleanup manager.
old-location: lwef\iemptyvolumecachecallback.htm
old-project: lwef
ms.assetid: d6775458-3b39-4ee8-90f9-d8a749bd1800
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEmptyVolumeCacheCallBack, IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features], IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features],described, _win32_IEmptyVolumeCacheCallBack, emptyvc/IEmptyVolumeCacheCallBack, lwef.iemptyvolumecachecallback, shell.iemptyvolumecachecallback
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
 - IEmptyVolumeCacheCallBack
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
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



