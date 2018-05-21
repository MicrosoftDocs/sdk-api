---
UID: NN:cscobj.IOfflineFilesFileSysInfo
title: IOfflineFilesFileSysInfo
author: windows-driver-content
description: Represents the standard information associated with a file system item in the Offline Files cache.
old-location: of\iofflinefilesfilesysinfo.htm
old-project: OfflineFiles
ms.assetid: d3da183d-eb12-4411-b461-b58689ef5bff
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: IOfflineFilesFileSysInfo, IOfflineFilesFileSysInfo interface [Offline Files], IOfflineFilesFileSysInfo interface [Offline Files],described, cscobj/IOfflineFilesFileSysInfo, of.iofflinefilesfilesysinfo
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
-	IOfflineFilesFileSysInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesFileSysInfo interface


## -description


Represents the standard information associated with a file system item in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesFileSysInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesFileSysInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesFileSysInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bf8a834-cd5e-46b9-9b7d-b5cc6fb9fe10">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the Win32 attributes for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a24b7126-ee9a-40f8-9fcd-8696e756a6b9">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/120b3f7c-6a92-4a03-8676-1ad4e4dc96b3">GetTimes</a>
</td>
<td align="left" width="63%">
Retrieves the time values associated with an item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

