---
UID: NF:cscobj.IOfflineFilesSuspendInfo.IsSuspended
title: IOfflineFilesSuspendInfo::IsSuspended (cscobj.h)
description: Determines whether an item is suspended.
helpviewer_keywords: ["IOfflineFilesSuspendInfo interface [Offline Files]","IsSuspended method","IOfflineFilesSuspendInfo.IsSuspended","IOfflineFilesSuspendInfo::IsSuspended","IsSuspended","IsSuspended method [Offline Files]","IsSuspended method [Offline Files]","IOfflineFilesSuspendInfo interface","cscobj/IOfflineFilesSuspendInfo::IsSuspended","of.iofflinefilessuspendinfo_issuspended"]
old-location: of\iofflinefilessuspendinfo_issuspended.htm
tech.root: of
ms.assetid: 6f29793f-3b34-4280-b375-3739aefd74db
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSuspendInfo interface [Offline Files],IsSuspended method, IOfflineFilesSuspendInfo.IsSuspended, IOfflineFilesSuspendInfo::IsSuspended, IsSuspended, IsSuspended method [Offline Files], IsSuspended method [Offline Files],IOfflineFilesSuspendInfo interface, cscobj/IOfflineFilesSuspendInfo::IsSuspended, of.iofflinefilessuspendinfo_issuspended
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
 - IOfflineFilesSuspendInfo::IsSuspended
 - cscobj/IOfflineFilesSuspendInfo::IsSuspended
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
 - IOfflineFilesSuspendInfo.IsSuspended
---

# IOfflineFilesSuspendInfo::IsSuspended


## -description

Determines whether an item is suspended.

If an item is suspended and is a suspended root, it was suspended by using the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessuspend-suspendroot">IOfflineFilesSuspend::SuspendRoot</a> method.  If an item is suspended but is not a suspended root, its suspension was inherited from a suspended root.

## -parameters

### -param pbSuspended [out]

Receives <b>TRUE</b> if the item is suspended, or <b>FALSE</b> otherwise.

### -param pbSuspendedRoot [out]

Receives <b>TRUE</b> if the item is a suspended root, or <b>FALSE</b> otherwise.  If the item is not suspended, this value is always <b>FALSE</b>.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessuspendinfo">IOfflineFilesSuspendInfo</a>