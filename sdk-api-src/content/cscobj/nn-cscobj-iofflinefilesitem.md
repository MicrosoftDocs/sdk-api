---
UID: NN:cscobj.IOfflineFilesItem
title: IOfflineFilesItem (cscobj.h)
description: Represents a single item in the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesItem","IOfflineFilesItem interface [Offline Files]","IOfflineFilesItem interface [Offline Files]","described","cscobj/IOfflineFilesItem","of.iofflinefilesitem"]
old-location: of\iofflinefilesitem.htm
tech.root: of
ms.assetid: 870cf4c4-e757-429d-b6cc-c136ed5aa10e
ms.date: 12/05/2018
ms.keywords: IOfflineFilesItem, IOfflineFilesItem interface [Offline Files], IOfflineFilesItem interface [Offline Files],described, cscobj/IOfflineFilesItem, of.iofflinefilesitem
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
 - IOfflineFilesItem
 - cscobj/IOfflineFilesItem
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
 - IOfflineFilesItem
---

# IOfflineFilesItem interface


## -description

Represents a single item in the Offline Files cache. The item may be a server, share, directory or file.  While each item type has a type-specific interface (for example, <a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesserveritem">IOfflineFilesServerItem</a>), this interface provides the functionality that is common to all items.

## -inheritance

The <b>IOfflineFilesItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesItem</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
