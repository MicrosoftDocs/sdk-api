---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyClosingDisc
title: IDiscMasterProgressEvents::NotifyClosingDisc (imapi.h)
description: Notifies the application that it is has started closing the disc. No further notifications are sent until the burn is finished.
helpviewer_keywords: ["IDiscMasterProgressEvents interface [IMAPI]","NotifyClosingDisc method","IDiscMasterProgressEvents.NotifyClosingDisc","IDiscMasterProgressEvents::NotifyClosingDisc","NotifyClosingDisc","NotifyClosingDisc method [IMAPI]","NotifyClosingDisc method [IMAPI]","IDiscMasterProgressEvents interface","_win32_idiscmasterprogressevents_notifyclosingdisc","base.idiscmasterprogressevents_notifyclosingdisc","imapi.idiscmasterprogressevents_notifyclosingdisc","imapi/IDiscMasterProgressEvents::NotifyClosingDisc"]
old-location: imapi\idiscmasterprogressevents_notifyclosingdisc.htm
tech.root: imapi
ms.assetid: 2eeccb4e-0e49-40a9-b659-f0784f921074
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyClosingDisc method, IDiscMasterProgressEvents.NotifyClosingDisc, IDiscMasterProgressEvents::NotifyClosingDisc, NotifyClosingDisc, NotifyClosingDisc method [IMAPI], NotifyClosingDisc method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifyclosingdisc, base.idiscmasterprogressevents_notifyclosingdisc, imapi.idiscmasterprogressevents_notifyclosingdisc, imapi/IDiscMasterProgressEvents::NotifyClosingDisc
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
 - IDiscMasterProgressEvents::NotifyClosingDisc
 - imapi/IDiscMasterProgressEvents::NotifyClosingDisc
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
 - IDiscMasterProgressEvents.NotifyClosingDisc
---

# IDiscMasterProgressEvents::NotifyClosingDisc


## -description

Notifies the application that it is has started closing the disc. No further notifications are sent until the burn is finished.

## -parameters

### -param nEstimatedSeconds [in]

Number of seconds from notification that IMAPI estimates it will take to close the disc.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a>