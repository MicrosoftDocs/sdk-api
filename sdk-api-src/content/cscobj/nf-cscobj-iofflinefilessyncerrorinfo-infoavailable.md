---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.InfoAvailable
title: IOfflineFilesSyncErrorInfo::InfoAvailable
author: windows-sdk-content
description: Indicates whether information was obtained for the local, remote, or original copy of the item during synchronization.
old-location: of\iofflinefilessyncerrorinfo_infoavailable.htm
tech.root: OfflineFiles
ms.assetid: f4a491fb-445b-4a90-9131-e0e5964154fa
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesSyncErrorInfo interface [Offline Files],InfoAvailable method, IOfflineFilesSyncErrorInfo.InfoAvailable, IOfflineFilesSyncErrorInfo::InfoAvailable, InfoAvailable, InfoAvailable method [Offline Files], InfoAvailable method [Offline Files],IOfflineFilesSyncErrorInfo interface, cscobj/IOfflineFilesSyncErrorInfo::InfoAvailable, of.iofflinefilessyncerrorinfo_infoavailable
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
 - IOfflineFilesSyncErrorInfo.InfoAvailable
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
- IOfflineFilesSyncErrorInfo.InfoAvailable
: 
---

# IOfflineFilesSyncErrorInfo::InfoAvailable


## -description


Indicates whether information was obtained for the local, remote, or original copy of the item during synchronization.


## -parameters




### -param pbLocalInfo [out]

Receives <b>TRUE</b> if information was obtained for the local copy of the item during synchronization, or <b>FALSE</b> otherwise.  If <b>TRUE</b>, <a href="https://msdn.microsoft.com/en-us/library/Bb530627(v=VS.85).aspx">GetLocalInfo</a> can be called to retrieve the information.


### -param pbRemoteInfo [out]

Receives <b>TRUE</b> if information was obtained for the remote copy of the item during synchronization, or <b>FALSE</b> otherwise.   If <b>TRUE</b>, <a href="https://msdn.microsoft.com/en-us/library/Bb530629(v=VS.85).aspx">GetRemoteInfo</a> can be called to retrieve the information.


### -param pbOriginalInfo [out]

Receives <b>TRUE</b> if information was obtained for the original copy of the item during synchronization, or <b>FALSE</b> otherwise.  If <b>TRUE</b>, <a href="https://msdn.microsoft.com/en-us/library/Bb530628(v=VS.85).aspx">GetOriginalInfo</a> can be called to retrieve the information.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530625(v=VS.85).aspx">IOfflineFilesSyncErrorInfo</a>
 

 

