---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyPnPActivity
title: IDiscMasterProgressEvents::NotifyPnPActivity (imapi.h)
description: Notifies the application that there is a change to the list of valid disc recorders. (For example, a USB CD-R driver is removed from the system.).
helpviewer_keywords: ["IDiscMasterProgressEvents interface [IMAPI]","NotifyPnPActivity method","IDiscMasterProgressEvents.NotifyPnPActivity","IDiscMasterProgressEvents::NotifyPnPActivity","NotifyPnPActivity","NotifyPnPActivity method [IMAPI]","NotifyPnPActivity method [IMAPI]","IDiscMasterProgressEvents interface","_win32_idiscmasterprogressevents_notifypnpactivity","base.idiscmasterprogressevents_notifypnpactivity","imapi.idiscmasterprogressevents_notifypnpactivity","imapi/IDiscMasterProgressEvents::NotifyPnPActivity"]
old-location: imapi\idiscmasterprogressevents_notifypnpactivity.htm
tech.root: imapi
ms.assetid: d2b41e86-2f1b-46f1-955d-7fc42f8189a4
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyPnPActivity method, IDiscMasterProgressEvents.NotifyPnPActivity, IDiscMasterProgressEvents::NotifyPnPActivity, NotifyPnPActivity, NotifyPnPActivity method [IMAPI], NotifyPnPActivity method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifypnpactivity, base.idiscmasterprogressevents_notifypnpactivity, imapi.idiscmasterprogressevents_notifypnpactivity, imapi/IDiscMasterProgressEvents::NotifyPnPActivity
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
 - IDiscMasterProgressEvents::NotifyPnPActivity
 - imapi/IDiscMasterProgressEvents::NotifyPnPActivity
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
 - IDiscMasterProgressEvents.NotifyPnPActivity
---

# IDiscMasterProgressEvents::NotifyPnPActivity


## -description

Notifies the application that there is a change to the list of valid disc recorders. (For example, a USB CD-R driver is removed from the system.)



## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

An application should respond by calling 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-enumdiscrecorders">IDiscMaster::EnumDiscRecorders</a> to update its list of valid recorders. If the current active recorder has been invalidated, then a new recorder should be chosen.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a>
