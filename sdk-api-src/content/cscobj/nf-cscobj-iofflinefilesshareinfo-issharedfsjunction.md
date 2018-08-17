---
UID: NF:cscobj.IOfflineFilesShareInfo.IsShareDfsJunction
title: IOfflineFilesShareInfo::IsShareDfsJunction
author: windows-sdk-content
description: Determines whether the share item is a DFS junction or a shared folder on a server.
old-location: of\iofflinefilesshareinfo_issharedfsjunction.htm
old-project: offlinefiles
ms.assetid: fdb29270-2fe5-4313-afd9-c21b82b1949a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesShareInfo interface [Offline Files],IsShareDfsJunction method, IOfflineFilesShareInfo.IsShareDfsJunction, IOfflineFilesShareInfo::IsShareDfsJunction, IsShareDfsJunction, IsShareDfsJunction method [Offline Files], IsShareDfsJunction method [Offline Files],IOfflineFilesShareInfo interface, cscobj/IOfflineFilesShareInfo::IsShareDfsJunction, of.iofflinefilesshareinfo_issharedfsjunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IOfflineFilesShareInfo.IsShareDfsJunction
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesShareInfo::IsShareDfsJunction


## -description


Determines whether the share item is a DFS junction or a shared folder on a server.


## -parameters




### -param pbIsDfsJunction [out]

Receives <b>TRUE</b> if the item is a DFS junction, or <b>FALSE</b> if the share is a shared folder (\\server\share) on a server.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530611(v=VS.85).aspx">IOfflineFilesShareInfo</a>
 

 

