---
UID: NN:cscobj.IOfflineFilesSuspend
title: IOfflineFilesSuspend (cscobj.h)
description: Suspends or releases a share root or directory tree in the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesSuspend","IOfflineFilesSuspend interface [Offline Files]","IOfflineFilesSuspend interface [Offline Files]","described","cscobj/IOfflineFilesSuspend","of.iofflinefilessuspend"]
old-location: of\iofflinefilessuspend.htm
tech.root: of
ms.assetid: 697018c4-7cce-480a-b078-993cdac32bf5
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSuspend, IOfflineFilesSuspend interface [Offline Files], IOfflineFilesSuspend interface [Offline Files],described, cscobj/IOfflineFilesSuspend, of.iofflinefilessuspend
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
 - IOfflineFilesSuspend
 - cscobj/IOfflineFilesSuspend
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
 - IOfflineFilesSuspend
---

# IOfflineFilesSuspend interface


## -description

Suspends or releases a share root or directory tree in the Offline Files cache. A suspended tree is always offline and is never synchronized automatically by the Offline Files service.  It may, however, be synchronized by the user through Windows Explorer, through Sync Center, or by code calling the Offline Files API.

## -inheritance

The <b>IOfflineFilesSuspend</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesSuspend</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
