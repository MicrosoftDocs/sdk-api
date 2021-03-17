---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetRemoteInfo
title: IOfflineFilesSyncErrorInfo::GetRemoteInfo (cscobj.h)
description: Retrieves an instance of the IOfflineFilesSyncErrorItemInfo interface containing the file times, size, and attributes of the remote copy of the item involved in the synchronization.
helpviewer_keywords: ["GetRemoteInfo","GetRemoteInfo method [Offline Files]","GetRemoteInfo method [Offline Files]","IOfflineFilesSyncErrorInfo interface","IOfflineFilesSyncErrorInfo interface [Offline Files]","GetRemoteInfo method","IOfflineFilesSyncErrorInfo.GetRemoteInfo","IOfflineFilesSyncErrorInfo::GetRemoteInfo","cscobj/IOfflineFilesSyncErrorInfo::GetRemoteInfo","of.iofflinefilessyncerrorinfo_getremoteinfo"]
old-location: of\iofflinefilessyncerrorinfo_getremoteinfo.htm
tech.root: of
ms.assetid: 8b036680-b74c-485f-adae-88e59fc5e84c
ms.date: 12/05/2018
ms.keywords: GetRemoteInfo, GetRemoteInfo method [Offline Files], GetRemoteInfo method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetRemoteInfo method, IOfflineFilesSyncErrorInfo.GetRemoteInfo, IOfflineFilesSyncErrorInfo::GetRemoteInfo, cscobj/IOfflineFilesSyncErrorInfo::GetRemoteInfo, of.iofflinefilessyncerrorinfo_getremoteinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesSyncErrorInfo::GetRemoteInfo
 - cscobj/IOfflineFilesSyncErrorInfo::GetRemoteInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSyncErrorInfo.GetRemoteInfo
---

# IOfflineFilesSyncErrorInfo::GetRemoteInfo


## -description

Retrieves an instance of the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the remote copy of the item involved in the synchronization.

## -parameters

### -param ppInfo [out]

Receives the address of an instance of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> containing information about the remote item copy involved in the synchronization.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerrorinfo">IOfflineFilesSyncErrorInfo</a>