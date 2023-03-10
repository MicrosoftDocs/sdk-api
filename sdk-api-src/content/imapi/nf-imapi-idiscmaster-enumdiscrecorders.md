---
UID: NF:imapi.IDiscMaster.EnumDiscRecorders
title: IDiscMaster::EnumDiscRecorders (imapi.h)
description: Retrieves an enumerator for all disc recorders supported by the active disc master format.
helpviewer_keywords: ["EnumDiscRecorders","EnumDiscRecorders method [IMAPI]","EnumDiscRecorders method [IMAPI]","IDiscMaster interface","IDiscMaster interface [IMAPI]","EnumDiscRecorders method","IDiscMaster.EnumDiscRecorders","IDiscMaster::EnumDiscRecorders","_win32_idiscmaster_enumdiscrecorders","base.idiscmaster_enumdiscrecorders","imapi.idiscmaster_enumdiscrecorders","imapi/IDiscMaster::EnumDiscRecorders"]
old-location: imapi\idiscmaster_enumdiscrecorders.htm
tech.root: imapi
ms.assetid: 03daab81-11cf-4100-ab5e-3442a5972912
ms.date: 12/05/2018
ms.keywords: EnumDiscRecorders, EnumDiscRecorders method [IMAPI], EnumDiscRecorders method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],EnumDiscRecorders method, IDiscMaster.EnumDiscRecorders, IDiscMaster::EnumDiscRecorders, _win32_idiscmaster_enumdiscrecorders, base.idiscmaster_enumdiscrecorders, imapi.idiscmaster_enumdiscrecorders, imapi/IDiscMaster::EnumDiscRecorders
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
 - IDiscMaster::EnumDiscRecorders
 - imapi/IDiscMaster::EnumDiscRecorders
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
 - IDiscMaster.EnumDiscRecorders
---

# IDiscMaster::EnumDiscRecorders


## -description

Retrieves an enumerator for all disc recorders supported by the active disc master format.

## -parameters

### -param ppEnum [out]

Address of a pointer to the <b>IEnumDiscRecorders</b> enumerator.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

<b>IEnumDiscRecorders</b> is a standard COM enumerator, as documented in 
<b>IEnumXXXX</b>. Each call to <b>Next</b> returns an array of pointers to 
<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>. Each recorder interface represents a single available recorder already associated with an underlying physical disc recorder.

The list of available recorders may change due to Plug and Play arrivals or departures, or a call to 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscmasterformat">SetActiveDiscMasterFormat</a>. An application is notified of these changes when it receives a call to 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmasterprogressevents-notifypnpactivity">IDiscMasterProgressEvents::NotifyPnPActivity</a>. When a change occurs, the application should call this method again to retrieve a new enumerator, because each enumerator contains a snapshot of the devices supported at the time of the enumeration.

When a device is removed, its pointer and 
<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a> interface must remain valid even though the underlying physical device is missing. In this case, operations on an 
<b>IDiscRecorder</b> or a request to record a disc may return IMAPI_E_DEVICE_NOTPRESENT.

The <b>MaxWriteSpeed</b> property is updated when this method is called. The default setting is the highest available write speed.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>