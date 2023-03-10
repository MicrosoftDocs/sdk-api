---
UID: NN:cscobj.IOfflineFilesProgress
title: IOfflineFilesProgress (cscobj.h)
description: Used to report progress back to callers of lengthy Offline Files operations. (IOfflineFilesProgress)
helpviewer_keywords: ["IOfflineFilesProgress","IOfflineFilesProgress interface [Offline Files]","IOfflineFilesProgress interface [Offline Files]","described","cscobj/IOfflineFilesProgress","of.iofflinefilesprogress"]
old-location: of\iofflinefilesprogress.htm
tech.root: of
ms.assetid: b568a8c6-119b-486e-94e3-fe4e54a395bb
ms.date: 12/05/2018
ms.keywords: IOfflineFilesProgress, IOfflineFilesProgress interface [Offline Files], IOfflineFilesProgress interface [Offline Files],described, cscobj/IOfflineFilesProgress, of.iofflinefilesprogress
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
 - IOfflineFilesProgress
 - cscobj/IOfflineFilesProgress
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
 - IOfflineFilesProgress
---

# IOfflineFilesProgress interface


## -description

Used to report progress back to callers of lengthy Offline Files operations. This interface provides the most basic "begin" and "end" notifications.  It is used as a base interface for all other progress interfaces.

## -inheritance

The <b>IOfflineFilesProgress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesProgress</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
