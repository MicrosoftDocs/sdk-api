---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyTrackProgress
title: IDiscMasterProgressEvents::NotifyTrackProgress (imapi.h)
description: Notifies an application that a track has started or finished during the burn of an audio disc.
helpviewer_keywords: ["IDiscMasterProgressEvents interface [IMAPI]","NotifyTrackProgress method","IDiscMasterProgressEvents.NotifyTrackProgress","IDiscMasterProgressEvents::NotifyTrackProgress","NotifyTrackProgress","NotifyTrackProgress method [IMAPI]","NotifyTrackProgress method [IMAPI]","IDiscMasterProgressEvents interface","_win32_idiscmasterprogressevents_notifytrackprogress","base.idiscmasterprogressevents_notifytrackprogress","imapi.idiscmasterprogressevents_notifytrackprogress","imapi/IDiscMasterProgressEvents::NotifyTrackProgress"]
old-location: imapi\idiscmasterprogressevents_notifytrackprogress.htm
tech.root: imapi
ms.assetid: fb1eafe9-d907-4b41-8e4d-03f1b3f51012
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyTrackProgress method, IDiscMasterProgressEvents.NotifyTrackProgress, IDiscMasterProgressEvents::NotifyTrackProgress, NotifyTrackProgress, NotifyTrackProgress method [IMAPI], NotifyTrackProgress method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifytrackprogress, base.idiscmasterprogressevents_notifytrackprogress, imapi.idiscmasterprogressevents_notifytrackprogress, imapi/IDiscMasterProgressEvents::NotifyTrackProgress
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
 - IDiscMasterProgressEvents::NotifyTrackProgress
 - imapi/IDiscMasterProgressEvents::NotifyTrackProgress
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
 - IDiscMasterProgressEvents.NotifyTrackProgress
---

# IDiscMasterProgressEvents::NotifyTrackProgress


## -description

Notifies an application that a track has started or finished  during the burn of an audio disc.

## -parameters

### -param nCurrentTrack [in]

Number of tracks that have been completely burned.

### -param nTotalTracks [in]

Total number of tracks that must be burned.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

The notification for zero out of <i>nTotalTracks</i> indicates the start of track 1. The notification for track N out of <i>nTotalTracks</i> indicates that track N is complete and track N+1 is beginning. Finally, the notification for <i>nTotalTracks</i> out of <i>nTotalTracks</i> indicates the last track has been written.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a>