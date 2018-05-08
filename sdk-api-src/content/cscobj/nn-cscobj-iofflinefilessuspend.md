---
UID: NN:cscobj.IOfflineFilesSuspend
title: IOfflineFilesSuspend
author: windows-driver-content
description: Suspends or releases a share root or directory tree in the Offline Files cache.
old-location: of\iofflinefilessuspend.htm
old-project: OfflineFiles
ms.assetid: 697018c4-7cce-480a-b078-993cdac32bf5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOfflineFilesSuspend, IOfflineFilesSuspend interface [Offline Files], IOfflineFilesSuspend interface [Offline Files],described, cscobj/IOfflineFilesSuspend, of.iofflinefilessuspend
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IOfflineFilesSuspend
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSuspend interface


## -description



    Suspends or releases a share root or directory tree in the Offline Files cache. A suspended tree is always offline and is never synchronized automatically by the Offline Files service.  It may, however, be synchronized by the user through Windows Explorer, through Sync Center, or by code calling the Offline Files API.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSuspend</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesSuspend</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSuspend</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5307bc8c-e6e9-4ae7-b2da-036fc9c5c08d">SuspendRoot</a>
</td>
<td align="left" width="63%">
Suspend or release a share root or directory tree.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

