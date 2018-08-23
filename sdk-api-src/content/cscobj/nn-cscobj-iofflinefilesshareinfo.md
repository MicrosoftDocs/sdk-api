---
UID: NN:cscobj.IOfflineFilesShareInfo
title: IOfflineFilesShareInfo
author: windows-sdk-content
description: Presents share-specific information about cached items.
old-location: of\iofflinefilesshareinfo.htm
old-project: offlinefiles
ms.assetid: 9647aae3-06ca-4813-8243-3d0fb794802d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesShareInfo, IOfflineFilesShareInfo interface [Offline Files], IOfflineFilesShareInfo interface [Offline Files],described, cscobj/IOfflineFilesShareInfo, of.iofflinefilesshareinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesShareInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesShareInfo interface


## -description


Presents share-specific information about cached items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesShareInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesShareInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesShareInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530612(v=VS.85).aspx">GetShareCachingMode</a>
</td>
<td align="left" width="63%">
Retrieves the caching mode configuration of the closest ancestor share to the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530613(v=VS.85).aspx">GetShareItem</a>
</td>
<td align="left" width="63%">
Finds the cache item representing the closest ancestor share to the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530614(v=VS.85).aspx">IsShareDfsJunction</a>
</td>
<td align="left" width="63%">
Determines whether the share item is a DFS junction or a shared folder on a server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

