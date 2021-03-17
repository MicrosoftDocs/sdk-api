---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetOriginalInfo
title: IOfflineFilesSyncErrorInfo::GetOriginalInfo (cscobj.h)
description: Retrieves an instance of the IOfflineFilesSyncErrorItemInfo interface containing the file times, size, and attributes of the original copy of the item involved in the synchronization.
helpviewer_keywords: ["GetOriginalInfo","GetOriginalInfo method [Offline Files]","GetOriginalInfo method [Offline Files]","IOfflineFilesSyncErrorInfo interface","IOfflineFilesSyncErrorInfo interface [Offline Files]","GetOriginalInfo method","IOfflineFilesSyncErrorInfo.GetOriginalInfo","IOfflineFilesSyncErrorInfo::GetOriginalInfo","cscobj/IOfflineFilesSyncErrorInfo::GetOriginalInfo","of.iofflinefilessyncerrorinfo_getoriginalinfo"]
old-location: of\iofflinefilessyncerrorinfo_getoriginalinfo.htm
tech.root: of
ms.assetid: 1cf3a21c-5ae1-475c-9eb7-2d520ee2ce79
ms.date: 12/05/2018
ms.keywords: GetOriginalInfo, GetOriginalInfo method [Offline Files], GetOriginalInfo method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetOriginalInfo method, IOfflineFilesSyncErrorInfo.GetOriginalInfo, IOfflineFilesSyncErrorInfo::GetOriginalInfo, cscobj/IOfflineFilesSyncErrorInfo::GetOriginalInfo, of.iofflinefilessyncerrorinfo_getoriginalinfo
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
 - IOfflineFilesSyncErrorInfo::GetOriginalInfo
 - cscobj/IOfflineFilesSyncErrorInfo::GetOriginalInfo
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
 - IOfflineFilesSyncErrorInfo.GetOriginalInfo
---

# IOfflineFilesSyncErrorInfo::GetOriginalInfo


## -description

Retrieves an instance of the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the original copy of the item involved in the synchronization.

"Original" refers to the state information recorded the last time the cached item was in sync with the server.

## -parameters

### -param ppInfo [out]

Receives the address of an instance of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> containing information about the original item copy involved in the synchronization.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerrorinfo">IOfflineFilesSyncErrorInfo</a>