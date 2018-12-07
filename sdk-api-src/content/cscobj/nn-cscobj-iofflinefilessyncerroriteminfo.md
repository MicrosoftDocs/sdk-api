---
UID: NN:cscobj.IOfflineFilesSyncErrorItemInfo
title: IOfflineFilesSyncErrorItemInfo
author: windows-sdk-content
description: Provides file attributes, time information, and file size for an item associated with a sync error.
old-location: of\iofflinefilessyncerroriteminfo.htm
tech.root: offlinefiles
ms.assetid: 0af039a6-f0dd-4117-a174-38d32cfc0220
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesSyncErrorItemInfo, IOfflineFilesSyncErrorItemInfo interface [Offline Files], IOfflineFilesSyncErrorItemInfo interface [Offline Files],described, cscobj/IOfflineFilesSyncErrorItemInfo, of.iofflinefilessyncerroriteminfo
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
 - IOfflineFilesSyncErrorItemInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSyncErrorItemInfo interface


## -description


Provides file attributes, time information, and file size for an item associated with a sync error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncErrorItemInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesSyncErrorItemInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb530634(v=VS.85).aspx">GetFileAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the Win32 file attributes for the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530635(v=VS.85).aspx">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the item in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530636(v=VS.85).aspx">GetFileTimes</a>
</td>
<td align="left" width="63%">
Retrieves the last-write and change times for the item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

