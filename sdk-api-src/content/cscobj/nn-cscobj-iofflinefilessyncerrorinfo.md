---
UID: NN:cscobj.IOfflineFilesSyncErrorInfo
title: IOfflineFilesSyncErrorInfo (cscobj.h)
author: windows-sdk-content
description: Supplied with the IOfflineFilesSyncProgress::SyncItemResult method to communicate details about the item that experienced a sync error.
old-location: of\iofflinefilessyncerrorinfo.htm
tech.root: offlinefiles
ms.assetid: df1dd351-eb18-46e6-b778-852f551adfd1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncErrorInfo, IOfflineFilesSyncErrorInfo interface [Offline Files], IOfflineFilesSyncErrorInfo interface [Offline Files],described, cscobj/IOfflineFilesSyncErrorInfo, of.iofflinefilessyncerrorinfo
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
 - IOfflineFilesSyncErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSyncErrorInfo interface


## -description


Supplied with the <a href="https://msdn.microsoft.com/2a93d52e-6b91-4d91-9372-5f0718621841">IOfflineFilesSyncProgress::SyncItemResult</a> method to communicate details about the item that experienced a sync error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncErrorInfo</b> interface inherits from <a href="https://msdn.microsoft.com/6c78d475-aa63-49e4-863f-1a197801f2f9">IOfflineFilesErrorInfo</a>. <b>IOfflineFilesSyncErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1014e42f-83af-493e-b264-a46055f646a5">GetItemChangeFlags</a>
</td>
<td align="left" width="63%">
Retrieves a value containing a set of flags that describe what changes were encountered during the sync operation associated with the sync error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53e03524-9cb6-4b91-8b2a-bf428a16140e">GetLocalInfo</a>
</td>
<td align="left" width="63%">
Retrieves an instance of the <a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the local copy of the item involved in the synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cf3a21c-5ae1-475c-9eb7-2d520ee2ce79">GetOriginalInfo</a>
</td>
<td align="left" width="63%">
Retrieves an instance of the <a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the original copy of the item involved in the synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b036680-b74c-485f-adae-88e59fc5e84c">GetRemoteInfo</a>
</td>
<td align="left" width="63%">
Retrieves an instance of the <a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the remote copy of the item involved in the synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21973fb8-26f9-40a0-bb9a-d9c5ff6924e7">GetSyncOperation</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the type of sync operation being performed when the error was encountered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4a491fb-445b-4a90-9131-e0e5964154fa">InfoAvailable</a>
</td>
<td align="left" width="63%">
Indicates whether information was obtained for the local, remote, or original copy of the item during synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2e8ae5b-92e7-4284-a02f-6eb3ab288376">InfoEnumerated</a>
</td>
<td align="left" width="63%">
Indicates whether information was queried for the local, remote, or original copy of the item during synchronization.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6c78d475-aa63-49e4-863f-1a197801f2f9">IOfflineFilesErrorInfo</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

