---
UID: NF:cscobj.IOfflineFilesSuspendInfo.IsSuspended
title: IOfflineFilesSuspendInfo::IsSuspended
author: windows-sdk-content
description: Determines whether an item is suspended.
old-location: of\iofflinefilessuspendinfo_issuspended.htm
old-project: offlinefiles
ms.assetid: 6f29793f-3b34-4280-b375-3739aefd74db
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesSuspendInfo interface [Offline Files],IsSuspended method, IOfflineFilesSuspendInfo.IsSuspended, IOfflineFilesSuspendInfo::IsSuspended, IsSuspended, IsSuspended method [Offline Files], IsSuspended method [Offline Files],IOfflineFilesSuspendInfo interface, cscobj/IOfflineFilesSuspendInfo::IsSuspended, of.iofflinefilessuspendinfo_issuspended
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
 - IOfflineFilesSuspendInfo.IsSuspended
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSuspendInfo::IsSuspended


## -description


Determines whether an item is suspended.

If an item is suspended and is a suspended root, it was suspended by using the <a href="https://msdn.microsoft.com/en-us/library/Bb530622(v=VS.85).aspx">IOfflineFilesSuspend::SuspendRoot</a> method.  If an item is suspended but is not a suspended root, its suspension was inherited from a suspended root.


## -parameters




### -param pbSuspended [out]

Receives <b>TRUE</b> if the item is suspended, or <b>FALSE</b> otherwise.


### -param pbSuspendedRoot [out]

Receives <b>TRUE</b> if the item is a suspended root, or <b>FALSE</b> otherwise.  If the item is not suspended, this value is always <b>FALSE</b>.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530620(v=VS.85).aspx">IOfflineFilesSuspendInfo</a>
 

 

