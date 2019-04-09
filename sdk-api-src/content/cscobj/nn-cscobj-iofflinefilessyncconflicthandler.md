---
UID: NN:cscobj.IOfflineFilesSyncConflictHandler
title: IOfflineFilesSyncConflictHandler (cscobj.h)
author: windows-sdk-content
description: Used by a client calling the IOfflineFilesCache::Synchronize method to prescribe a conflict resolution strategy for sync conflicts as they are detected.
old-location: of\iofflinefilessyncconflicthandler.htm
tech.root: offlinefiles
ms.assetid: f3d5ed0e-727d-43e1-9d29-2a0a71bb8a64
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncConflictHandler, IOfflineFilesSyncConflictHandler interface [Offline Files], IOfflineFilesSyncConflictHandler interface [Offline Files],described, cscobj/IOfflineFilesSyncConflictHandler, of.iofflinefilessyncconflicthandler
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSyncConflictHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSyncConflictHandler interface


## -description


Used by a client calling the <a href="https://msdn.microsoft.com/4a9dd105-ea68-40ce-b1cb-6126ca932095">IOfflineFilesCache::Synchronize</a> method to prescribe a conflict resolution strategy for sync conflicts as they are detected.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncConflictHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesSyncConflictHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncConflictHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb6fbdcf-1833-4ada-880e-f2dbfce64d99">ResolveConflict</a>
</td>
<td align="left" width="63%">
Provides a resolution decision for a sync conflict.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

