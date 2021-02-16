---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyBurnComplete
title: IDiscMasterProgressEvents::NotifyBurnComplete (imapi.h)
description: Notifies an application that a call to IDiscMaster::RecordDisc has finished.
helpviewer_keywords: ["IDiscMasterProgressEvents interface [IMAPI]","NotifyBurnComplete method","IDiscMasterProgressEvents.NotifyBurnComplete","IDiscMasterProgressEvents::NotifyBurnComplete","NotifyBurnComplete","NotifyBurnComplete method [IMAPI]","NotifyBurnComplete method [IMAPI]","IDiscMasterProgressEvents interface","_win32_idiscmasterprogressevents_notifyburncomplete","base.idiscmasterprogressevents_notifyburncomplete","imapi.idiscmasterprogressevents_notifyburncomplete","imapi/IDiscMasterProgressEvents::NotifyBurnComplete"]
old-location: imapi\idiscmasterprogressevents_notifyburncomplete.htm
tech.root: imapi
ms.assetid: deefe7cb-60aa-4255-a7b1-261fb40e6318
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyBurnComplete method, IDiscMasterProgressEvents.NotifyBurnComplete, IDiscMasterProgressEvents::NotifyBurnComplete, NotifyBurnComplete, NotifyBurnComplete method [IMAPI], NotifyBurnComplete method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifyburncomplete, base.idiscmasterprogressevents_notifyburncomplete, imapi.idiscmasterprogressevents_notifyburncomplete, imapi/IDiscMasterProgressEvents::NotifyBurnComplete
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
 - IDiscMasterProgressEvents::NotifyBurnComplete
 - imapi/IDiscMasterProgressEvents::NotifyBurnComplete
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
 - IDiscMasterProgressEvents.NotifyBurnComplete
---

# IDiscMasterProgressEvents::NotifyBurnComplete


## -description

Notifies an application that a call to 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">IDiscMaster::RecordDisc</a> has finished.

## -parameters

### -param status [in]

Status code to be returned from 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">IDiscMaster::RecordDisc</a>.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a>