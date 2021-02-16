---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetLocalInfo
title: IOfflineFilesSyncErrorInfo::GetLocalInfo (cscobj.h)
description: Retrieves an instance of the IOfflineFilesSyncErrorItemInfo interface containing the file times, size, and attributes of the local copy of the item involved in the synchronization.
helpviewer_keywords: ["GetLocalInfo","GetLocalInfo method [Offline Files]","GetLocalInfo method [Offline Files]","IOfflineFilesSyncErrorInfo interface","IOfflineFilesSyncErrorInfo interface [Offline Files]","GetLocalInfo method","IOfflineFilesSyncErrorInfo.GetLocalInfo","IOfflineFilesSyncErrorInfo::GetLocalInfo","cscobj/IOfflineFilesSyncErrorInfo::GetLocalInfo","of.iofflinefilessyncerrorinfo_getlocalinfo"]
old-location: of\iofflinefilessyncerrorinfo_getlocalinfo.htm
tech.root: of
ms.assetid: 53e03524-9cb6-4b91-8b2a-bf428a16140e
ms.date: 12/05/2018
ms.keywords: GetLocalInfo, GetLocalInfo method [Offline Files], GetLocalInfo method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetLocalInfo method, IOfflineFilesSyncErrorInfo.GetLocalInfo, IOfflineFilesSyncErrorInfo::GetLocalInfo, cscobj/IOfflineFilesSyncErrorInfo::GetLocalInfo, of.iofflinefilessyncerrorinfo_getlocalinfo
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
 - IOfflineFilesSyncErrorInfo::GetLocalInfo
 - cscobj/IOfflineFilesSyncErrorInfo::GetLocalInfo
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
 - IOfflineFilesSyncErrorInfo.GetLocalInfo
---

# IOfflineFilesSyncErrorInfo::GetLocalInfo


## -description

Retrieves an instance of the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the local copy of the item involved in the synchronization.

## -parameters

### -param ppInfo [out]

Receives the address of an instance of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> containing information about the local item copy involved in the synchronization.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerrorinfo">IOfflineFilesSyncErrorInfo</a>