---
UID: NN:cscobj.IOfflineFilesCache2
title: IOfflineFilesCache2
author: windows-driver-content
description: Implements the RenameItemEx method.
old-location: of\iofflinefilescache2.htm
old-project: OfflineFiles
ms.assetid: B4E2C2B0-AA6B-4657-8711-E5057720AF15
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IOfflineFilesCache2, IOfflineFilesCache2 interface [Offline Files], IOfflineFilesCache2 interface [Offline Files],described, cscobj/IOfflineFilesCache2, of.iofflinefilescache2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1
req.target-min-winversvr: Windows Server 2008 R2 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesCache2
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesCache2 interface


## -description


Implements the <a href="https://msdn.microsoft.com/766ABFE7-4417-47BA-ADF2-AA876C3A868A">RenameItemEx</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesCache2</b> interface inherits from <a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>. <b>IOfflineFilesCache2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesCache2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/766ABFE7-4417-47BA-ADF2-AA876C3A868A">RenameItemEx</a>
</td>
<td align="left" width="63%">
Renames an item in the cache. This method is identical to the <a href="https://msdn.microsoft.com/883f29cb-d551-4358-8e74-f901956d8829">IOfflineFilesCache::RenameItem</a> method, except that it will attempt to do the rename operation right away.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

