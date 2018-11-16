---
UID: NN:cscobj.IOfflineFilesSyncProgress
title: IOfflineFilesSyncProgress
author: windows-sdk-content
description: Used to report progress back to the caller during synchronization and synchronization-related operations.
old-location: of\iofflinefilessyncprogress.htm
tech.root: OfflineFiles
ms.assetid: 7fc5ff29-be9d-4fad-96a8-94058bb708fa
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesSyncProgress, IOfflineFilesSyncProgress interface [Offline Files], IOfflineFilesSyncProgress interface [Offline Files],described, cscobj/IOfflineFilesSyncProgress, of.iofflinefilessyncprogress
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
 - IOfflineFilesSyncProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSyncProgress interface


## -description


Used to report progress back to the caller during synchronization and 
    synchronization-related operations. This interface inherits from 
    <a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>.  For a description of 
    inherited methods, see 
    <a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncProgress</b> interface inherits from <a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>. <b>IOfflineFilesSyncProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1cdbc30-bcc9-4023-a3a2-070fb9958609">SyncItemBegin</a>
</td>
<td align="left" width="63%">
Reports that a synchronization operation on an item is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a93d52e-6b91-4d91-9372-5f0718621841">SyncItemResult</a>
</td>
<td align="left" width="63%">
Reports that an item has been processed during the synchronization operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

