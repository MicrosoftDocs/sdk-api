---
UID: NF:cscobj.IOfflineFilesCache2.RenameItemEx
title: IOfflineFilesCache2::RenameItemEx
author: windows-sdk-content
description: Renames an item in the cache. This method is identical to the IOfflineFilesCache::RenameItem method, except that it will attempt to do the rename operation right away.
old-location: of\iofflinefilescache2_renameitemex.htm
tech.root: offlinefiles
ms.assetid: 766ABFE7-4417-47BA-ADF2-AA876C3A868A
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesCache2 interface [Offline Files],RenameItemEx method, IOfflineFilesCache2.RenameItemEx, IOfflineFilesCache2::RenameItemEx, RenameItemEx, RenameItemEx method [Offline Files], RenameItemEx method [Offline Files],IOfflineFilesCache2 interface, cscobj/IOfflineFilesCache2::RenameItemEx, of.iofflinefilescache2_renameitemex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IOfflineFilesCache2.RenameItemEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesCache2::RenameItemEx


## -description


Renames an item in the cache. This method is identical to the <a href="https://msdn.microsoft.com/en-us/library/Bb530500(v=VS.85).aspx">IOfflineFilesCache::RenameItem</a> method, except that it will attempt to do the rename operation right away. 


## -parameters




### -param pszPathOriginal [in]

Fully qualified UNC path of the item (server, share, file or directory) to be renamed.


### -param pszPathNew [in]

The new path to replace <i>pszPathOriginal</i> if the item that  <i>pszPathOriginal</i> points to exists in the cache.


### -param bReplaceIfExists [in]

This parameter is reserved for future use.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This method does not require system administrator privilege.

If the item to be renamed is a file or directory, it must obey the file system semantics for the rename operation. If the file or a child file (for a directory) is already open, the rename will fail. Also, this method attempts to perform the rename as long as the user has access to the item that is being renamed.

If you need to minimize the chance that the item is in use, call the <a href="https://msdn.microsoft.com/en-us/library/Bb530500(v=VS.85).aspx">IOfflineFilesCache::RenameItem</a> method instead.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh769076(v=VS.85).aspx">IOfflineFilesCache2</a>
 

 

