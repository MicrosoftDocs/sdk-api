---
UID: NN:cscobj.IOfflineFilesSyncErrorItemInfo
title: IOfflineFilesSyncErrorItemInfo
author: windows-sdk-content
description: Provides file attributes, time information, and file size for an item associated with a sync error.
old-location: of\iofflinefilessyncerroriteminfo.htm
old-project: OfflineFiles
ms.assetid: 0af039a6-f0dd-4117-a174-38d32cfc0220
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IOfflineFilesSyncErrorItemInfo, IOfflineFilesSyncErrorItemInfo interface [Offline Files], IOfflineFilesSyncErrorItemInfo interface [Offline Files],described, cscobj/IOfflineFilesSyncErrorItemInfo, of.iofflinefilessyncerroriteminfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IOfflineFilesSyncErrorItemInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSyncErrorItemInfo interface


## -description


Provides file attributes, time information, and file size for an item associated with a sync error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncErrorItemInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesSyncErrorItemInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncErrorItemInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e14d571-230b-4757-8e81-2fb8dc6b9c3f">GetFileAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the Win32 file attributes for the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1873a10-0e60-46c3-a3a3-12d974cc0ee9">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the item in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dec0ce0c-ef24-482f-9890-19864d9ff652">GetFileTimes</a>
</td>
<td align="left" width="63%">
Retrieves the last-write and change times for the item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

