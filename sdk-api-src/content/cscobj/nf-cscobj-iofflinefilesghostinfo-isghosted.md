---
UID: NF:cscobj.IOfflineFilesGhostInfo.IsGhosted
title: IOfflineFilesGhostInfo::IsGhosted
author: windows-sdk-content
description: Determines whether the item is ghosted.
old-location: of\iofflinefilesghostinfo_isghosted.htm
tech.root: offlinefiles
ms.assetid: b2e8ca73-4186-4971-b5be-41ecfc6b5e4a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesGhostInfo interface [Offline Files],IsGhosted method, IOfflineFilesGhostInfo.IsGhosted, IOfflineFilesGhostInfo::IsGhosted, IsGhosted, IsGhosted method [Offline Files], IsGhosted method [Offline Files],IOfflineFilesGhostInfo interface, cscobj/IOfflineFilesGhostInfo::IsGhosted, of.iofflinefilesghostinfo_isghosted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IOfflineFilesGhostInfo.IsGhosted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesGhostInfo::IsGhosted


## -description


Determines whether the item is ghosted.


## -parameters




### -param pbGhosted [out]

Receives <b>TRUE</b> if the item is ghosted, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



An item is said to be ghosted in the offline files cache if, when the item is offline, its name is visible to the user, but its contents are not accessible. A file or directory can be in this state for one of the following reasons:

<ul>
<li>The item is pinned, which means that there is an entry for it in the cache.  However, either the content has not yet been synchronized to the client, or it was removed from the client (due to loss of oplock or detection of stale data) when the client transitioned offline.</li>
<li>The item has a sibling file or directory that is the root of a pinned namespace in the cache. When an item is pinned, its sibling items are ghosted so that the user can still see where the pinned item and its siblings are located in the online namespace even if the sibling items are not available offline.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd941689(v=VS.85).aspx">IOfflineFilesGhostInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd941692(v=VS.85).aspx">IOfflineFilesPinInfo2::IsPartlyPinned</a>
 

 

