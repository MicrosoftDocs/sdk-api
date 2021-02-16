---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyBlockProgress
title: IDiscMasterProgressEvents::NotifyBlockProgress (imapi.h)
description: Notifies an application of its progress in burning a disc on the active recorder. Notifications are sent for the first and last blocks, and at points in between.
helpviewer_keywords: ["IDiscMasterProgressEvents interface [IMAPI]","NotifyBlockProgress method","IDiscMasterProgressEvents.NotifyBlockProgress","IDiscMasterProgressEvents::NotifyBlockProgress","NotifyBlockProgress","NotifyBlockProgress method [IMAPI]","NotifyBlockProgress method [IMAPI]","IDiscMasterProgressEvents interface","_win32_idiscmasterprogressevents_notifyblockprogress","base.idiscmasterprogressevents_notifyblockprogress","imapi.idiscmasterprogressevents_notifyblockprogress","imapi/IDiscMasterProgressEvents::NotifyBlockProgress"]
old-location: imapi\idiscmasterprogressevents_notifyblockprogress.htm
tech.root: imapi
ms.assetid: 6c156be7-5ba4-48e7-a0d1-b0b8d69b30e2
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyBlockProgress method, IDiscMasterProgressEvents.NotifyBlockProgress, IDiscMasterProgressEvents::NotifyBlockProgress, NotifyBlockProgress, NotifyBlockProgress method [IMAPI], NotifyBlockProgress method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifyblockprogress, base.idiscmasterprogressevents_notifyblockprogress, imapi.idiscmasterprogressevents_notifyblockprogress, imapi/IDiscMasterProgressEvents::NotifyBlockProgress
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscMasterProgressEvents::NotifyBlockProgress
 - imapi/IDiscMasterProgressEvents::NotifyBlockProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscMasterProgressEvents.NotifyBlockProgress
---

# IDiscMasterProgressEvents::NotifyBlockProgress


## -description

Notifies an application of its progress in burning a disc on the active recorder. Notifications are sent for the first and last blocks, and at points in between.

## -parameters

### -param nCompleted [in]

Number of blocks that have been burned onto a disc or track so far.

### -param nTotal [in]

Total number of blocks to be burned to finish a disc or track.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a>