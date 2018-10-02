---
UID: NN:cscobj.IOfflineFilesSyncProgress
title: IOfflineFilesSyncProgress
author: windows-sdk-content
description: Used to report progress back to the caller during synchronization and synchronization-related operations.
old-location: of\iofflinefilessyncprogress.htm
tech.root: OfflineFiles
ms.assetid: 7fc5ff29-be9d-4fad-96a8-94058bb708fa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesSyncProgress, IOfflineFilesSyncProgress interface [Offline Files], IOfflineFilesSyncProgress interface [Offline Files],described, cscobj/IOfflineFilesSyncProgress, of.iofflinefilessyncprogress
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
    <a href="https://msdn.microsoft.com/en-us/library/Bb530596(v=VS.85).aspx">IOfflineFilesProgress</a>.  For a description of 
    inherited methods, see 
    <a href="https://msdn.microsoft.com/en-us/library/Bb530596(v=VS.85).aspx">IOfflineFilesProgress</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncProgress</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb530596(v=VS.85).aspx">IOfflineFilesProgress</a>. <b>IOfflineFilesSyncProgress</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb530638(v=VS.85).aspx">SyncItemBegin</a>
</td>
<td align="left" width="63%">
Reports that a synchronization operation on an item is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530639(v=VS.85).aspx">SyncItemResult</a>
</td>
<td align="left" width="63%">
Reports that an item has been processed during the synchronization operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530596(v=VS.85).aspx">IOfflineFilesProgress</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

