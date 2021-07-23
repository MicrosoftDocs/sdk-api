---
UID: NN:cscobj.IOfflineFilesSyncConflictHandler
title: IOfflineFilesSyncConflictHandler (cscobj.h)
description: Used by a client calling the IOfflineFilesCache::Synchronize method to prescribe a conflict resolution strategy for sync conflicts as they are detected.
helpviewer_keywords: ["IOfflineFilesSyncConflictHandler","IOfflineFilesSyncConflictHandler interface [Offline Files]","IOfflineFilesSyncConflictHandler interface [Offline Files]","described","cscobj/IOfflineFilesSyncConflictHandler","of.iofflinefilessyncconflicthandler"]
old-location: of\iofflinefilessyncconflicthandler.htm
tech.root: of
ms.assetid: f3d5ed0e-727d-43e1-9d29-2a0a71bb8a64
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncConflictHandler, IOfflineFilesSyncConflictHandler interface [Offline Files], IOfflineFilesSyncConflictHandler interface [Offline Files],described, cscobj/IOfflineFilesSyncConflictHandler, of.iofflinefilessyncconflicthandler
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
 - IOfflineFilesSyncConflictHandler
 - cscobj/IOfflineFilesSyncConflictHandler
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
 - IOfflineFilesSyncConflictHandler
---

# IOfflineFilesSyncConflictHandler interface


## -description

Used by a client calling the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a> method to prescribe a conflict resolution strategy for sync conflicts as they are detected.

## -inheritance

The <b>IOfflineFilesSyncConflictHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesSyncConflictHandler</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
