---
UID: NF:cscobj.IOfflineFilesShareInfo.GetShareItem
title: IOfflineFilesShareInfo::GetShareItem
author: windows-sdk-content
description: Finds the cache item representing the closest ancestor share to the item.
old-location: of\iofflinefilesshareinfo_getshareitem.htm
tech.root: OfflineFiles
ms.assetid: fd4f92fb-1147-4be4-a61d-04f2f371b6c6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetShareItem, GetShareItem method [Offline Files], GetShareItem method [Offline Files],IOfflineFilesShareInfo interface, IOfflineFilesShareInfo interface [Offline Files],GetShareItem method, IOfflineFilesShareInfo.GetShareItem, IOfflineFilesShareInfo::GetShareItem, cscobj/IOfflineFilesShareInfo::GetShareItem, of.iofflinefilesshareinfo_getshareitem
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
 - IOfflineFilesShareInfo.GetShareItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesShareInfo.GetShareItem
: 
---

# IOfflineFilesShareInfo::GetShareItem


## -description


Finds the cache item representing the closest ancestor share to the item. In non-DFS scenarios this can be the \\server\share at the top of the namespace.  In DFS scenarios this might be a cache directory entry that corresponds to a share in the DFS namespace.


## -parameters




### -param ppShareItem [out]

Receives the address of the <a href="https://msdn.microsoft.com/aff6be4a-07bc-4a74-8fbf-92fe8985f5b6">IOfflineFilesShareItem</a> interface on the share item.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530611(v=VS.85).aspx">IOfflineFilesShareInfo</a>
 

 

