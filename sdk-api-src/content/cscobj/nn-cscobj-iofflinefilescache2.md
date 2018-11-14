---
UID: NN:cscobj.IOfflineFilesCache2
title: IOfflineFilesCache2
author: windows-sdk-content
description: Implements the RenameItemEx method.
old-location: of\iofflinefilescache2.htm
tech.root: OfflineFiles
ms.assetid: B4E2C2B0-AA6B-4657-8711-E5057720AF15
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesCache2, IOfflineFilesCache2 interface [Offline Files], IOfflineFilesCache2 interface [Offline Files],described, cscobj/IOfflineFilesCache2, of.iofflinefilescache2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1
req.target-min-winversvr: Windows Server 2008 R2 with SP1
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
 - IOfflineFilesCache2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesCache2 interface


## -description


Implements the <a href="https://msdn.microsoft.com/en-us/library/Hh769077(v=VS.85).aspx">RenameItemEx</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesCache2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb530486(v=VS.85).aspx">IOfflineFilesCache</a>. <b>IOfflineFilesCache2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesCache2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh769077(v=VS.85).aspx">RenameItemEx</a>
</td>
<td align="left" width="63%">
Renames an item in the cache. This method is identical to the <a href="https://msdn.microsoft.com/en-us/library/Bb530500(v=VS.85).aspx">IOfflineFilesCache::RenameItem</a> method, except that it will attempt to do the rename operation right away.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530486(v=VS.85).aspx">IOfflineFilesCache</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

