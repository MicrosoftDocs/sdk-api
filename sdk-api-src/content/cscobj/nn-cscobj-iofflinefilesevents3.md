---
UID: NN:cscobj.IOfflineFilesEvents3
title: IOfflineFilesEvents3 (cscobj.h)
author: windows-sdk-content
description: Used to report events associated with transparently cached items.
old-location: of\iofflinefilesevents3.htm
tech.root: offlinefiles
ms.assetid: f68c2c0c-e4f7-4048-99c9-761f98928157
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents3, IOfflineFilesEvents3 interface [Offline Files], IOfflineFilesEvents3 interface [Offline Files],described, cscobj/IOfflineFilesEvents3, of.iofflinefilesevents3
ms.topic: interface
f1_keywords: 
 - "cscobj/IOfflineFilesEvents3"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesEvents3 interface


## -description


 Used to report events associated with transparently cached items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents3</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents2">IOfflineFilesEvents2</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>. <b>IOfflineFilesEvents3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents3-prefetchfilebegin">PrefetchFileBegin</a>
</td>
<td align="left" width="63%">
Reports that a file prefetch operation has begun.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents3-prefetchfileend">PrefetchFileEnd</a>
</td>
<td align="left" width="63%">
Reports that a file prefetch operation has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents3-transparentcacheitemnotify">TransparentCacheItemNotify</a>
</td>
<td align="left" width="63%">
Reports that an action has been performed on a transparently cached item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents2">IOfflineFilesEvents2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilestransparentcacheinfo">IOfflineFilesTransparentCacheInfo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

