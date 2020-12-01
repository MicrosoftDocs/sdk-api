---
UID: NF:imapi.IDiscMaster.GetActiveDiscRecorder
title: IDiscMaster::GetActiveDiscRecorder (imapi.h)
description: Retrieves an interface pointer to the active disc recorder. The active disc recorder is the recorder where a burn will occur when RecordDisc is called.
helpviewer_keywords: ["GetActiveDiscRecorder","GetActiveDiscRecorder method [IMAPI]","GetActiveDiscRecorder method [IMAPI]","IDiscMaster interface","IDiscMaster interface [IMAPI]","GetActiveDiscRecorder method","IDiscMaster.GetActiveDiscRecorder","IDiscMaster::GetActiveDiscRecorder","_win32_idiscmaster_getactivediscrecorder","base.idiscmaster_getactivediscrecorder","imapi.idiscmaster_getactivediscrecorder","imapi/IDiscMaster::GetActiveDiscRecorder"]
old-location: imapi\idiscmaster_getactivediscrecorder.htm
tech.root: imapi
ms.assetid: bdbc6108-c5c9-4083-84cd-7eae63d45c0f
ms.date: 12/05/2018
ms.keywords: GetActiveDiscRecorder, GetActiveDiscRecorder method [IMAPI], GetActiveDiscRecorder method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],GetActiveDiscRecorder method, IDiscMaster.GetActiveDiscRecorder, IDiscMaster::GetActiveDiscRecorder, _win32_idiscmaster_getactivediscrecorder, base.idiscmaster_getactivediscrecorder, imapi.idiscmaster_getactivediscrecorder, imapi/IDiscMaster::GetActiveDiscRecorder
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
 - IDiscMaster::GetActiveDiscRecorder
 - imapi/IDiscMaster::GetActiveDiscRecorder
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
 - IDiscMaster.GetActiveDiscRecorder
---

# IDiscMaster::GetActiveDiscRecorder


## -description

Retrieves an interface pointer to the active disc recorder. The active disc recorder is the recorder where a burn will occur when 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">RecordDisc</a> is called.

## -parameters

### -param ppRecorder [out]

Pointer to the 
<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a> interface of the currently selected disc recorder.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

There is no default active disc recorder. An application using this method must specifically select both an active mastering format and an active disc recorder before initiating a burn.

> [!NOTE]
> The active disc recorder can be invalidated by removing the device or changing the active disc mastering format. For example, a USB CD-R device may be disconnected from the machine while the application is still running (the application is alerted to this condition by a call to 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifypnpactivity">IDiscMasterProgressEvents::NotifyPnPActivity</a>). In either case, you must select a new active disc recorder.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>