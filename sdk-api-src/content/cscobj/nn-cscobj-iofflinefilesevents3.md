---
UID: NN:cscobj.IOfflineFilesEvents3
title: IOfflineFilesEvents3
author: windows-sdk-content
description: Used to report events associated with transparently cached items.
old-location: of\iofflinefilesevents3.htm
tech.root: offlinefiles
ms.assetid: f68c2c0c-e4f7-4048-99c9-761f98928157
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesEvents3, IOfflineFilesEvents3 interface [Offline Files], IOfflineFilesEvents3 interface [Offline Files],described, cscobj/IOfflineFilesEvents3, of.iofflinefilesevents3
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
 - IOfflineFilesEvents3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents3 interface


## -description


 Used to report events associated with transparently cached items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb530521(v=VS.85).aspx">IOfflineFilesEvents2</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>. <b>IOfflineFilesEvents3</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd442646(v=VS.85).aspx">PrefetchFileBegin</a>
</td>
<td align="left" width="63%">
Reports that a file prefetch operation has begun.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd442647(v=VS.85).aspx">PrefetchFileEnd</a>
</td>
<td align="left" width="63%">
Reports that a file prefetch operation has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd442648(v=VS.85).aspx">TransparentCacheItemNotify</a>
</td>
<td align="left" width="63%">
Reports that an action has been performed on a transparently cached item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530521(v=VS.85).aspx">IOfflineFilesEvents2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd442650(v=VS.85).aspx">IOfflineFilesTransparentCacheInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

