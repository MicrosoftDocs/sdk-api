---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.InfoAvailable
title: IOfflineFilesSyncErrorInfo::InfoAvailable (cscobj.h)
description: Indicates whether information was obtained for the local, remote, or original copy of the item during synchronization.
helpviewer_keywords: ["IOfflineFilesSyncErrorInfo interface [Offline Files]","InfoAvailable method","IOfflineFilesSyncErrorInfo.InfoAvailable","IOfflineFilesSyncErrorInfo::InfoAvailable","InfoAvailable","InfoAvailable method [Offline Files]","InfoAvailable method [Offline Files]","IOfflineFilesSyncErrorInfo interface","cscobj/IOfflineFilesSyncErrorInfo::InfoAvailable","of.iofflinefilessyncerrorinfo_infoavailable"]
old-location: of\iofflinefilessyncerrorinfo_infoavailable.htm
tech.root: of
ms.assetid: f4a491fb-445b-4a90-9131-e0e5964154fa
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncErrorInfo interface [Offline Files],InfoAvailable method, IOfflineFilesSyncErrorInfo.InfoAvailable, IOfflineFilesSyncErrorInfo::InfoAvailable, InfoAvailable, InfoAvailable method [Offline Files], InfoAvailable method [Offline Files],IOfflineFilesSyncErrorInfo interface, cscobj/IOfflineFilesSyncErrorInfo::InfoAvailable, of.iofflinefilessyncerrorinfo_infoavailable
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
 - IOfflineFilesSyncErrorInfo::InfoAvailable
 - cscobj/IOfflineFilesSyncErrorInfo::InfoAvailable
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
 - IOfflineFilesSyncErrorInfo.InfoAvailable
---

# IOfflineFilesSyncErrorInfo::InfoAvailable


## -description

Indicates whether information was obtained for the local, remote, or original copy of the item during synchronization.

## -parameters

### -param pbLocalInfo [out]

Receives <b>TRUE</b> if information was obtained for the local copy of the item during synchronization, or <b>FALSE</b> otherwise.  If <b>TRUE</b>, <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getlocalinfo">GetLocalInfo</a> can be called to retrieve the information.

### -param pbRemoteInfo [out]

Receives <b>TRUE</b> if information was obtained for the remote copy of the item during synchronization, or <b>FALSE</b> otherwise.   If <b>TRUE</b>, <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getremoteinfo">GetRemoteInfo</a> can be called to retrieve the information.

### -param pbOriginalInfo [out]

Receives <b>TRUE</b> if information was obtained for the original copy of the item during synchronization, or <b>FALSE</b> otherwise.  If <b>TRUE</b>, <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getoriginalinfo">GetOriginalInfo</a> can be called to retrieve the information.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerrorinfo">IOfflineFilesSyncErrorInfo</a>