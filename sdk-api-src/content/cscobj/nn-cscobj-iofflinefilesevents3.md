---
UID: NN:cscobj.IOfflineFilesEvents3
title: IOfflineFilesEvents3
author: windows-driver-content
description: Used to report events associated with transparently cached items.
old-location: of\iofflinefilesevents3.htm
old-project: OfflineFiles
ms.assetid: f68c2c0c-e4f7-4048-99c9-761f98928157
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOfflineFilesEvents3, IOfflineFilesEvents3 interface [Offline Files], IOfflineFilesEvents3 interface [Offline Files], described, cscobj/IOfflineFilesEvents3, of.iofflinefilesevents3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
-	IOfflineFilesEvents3
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents3 interface


## -description


 Used to report events associated with transparently cached items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents3</b> interface inherits from <a href="https://msdn.microsoft.com/746f7220-8c87-4218-bd97-ec9b862e549c">IOfflineFilesEvents2</a> and <a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>. <b>IOfflineFilesEvents3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesEvents3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b65354ed-dc4b-491c-9672-2f5fa91093bd">PrefetchFileBegin</a>
</td>
<td align="left" width="63%">
Reports that a file prefetch operation has begun.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5370d39-dd66-49c1-8774-cf335aa88e96">PrefetchFileEnd</a>
</td>
<td align="left" width="63%">
Reports that a file prefetch operation has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59bd7a71-0189-4c4d-a737-e6a3f09a533d">TransparentCacheItemNotify</a>
</td>
<td align="left" width="63%">
Reports that an action has been performed on a transparently cached item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>



<a href="https://msdn.microsoft.com/746f7220-8c87-4218-bd97-ec9b862e549c">IOfflineFilesEvents2</a>



<a href="https://msdn.microsoft.com/49c8213c-e8a1-4cb8-9b58-120fc0982b7b">IOfflineFilesTransparentCacheInfo</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

