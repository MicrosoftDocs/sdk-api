---
UID: NF:relogger.ITraceEvent.SetProviderId
title: ITraceEvent::SetProviderId (relogger.h)
description: Sets the GUID for the provider which traced an event.
helpviewer_keywords: ["ITraceEvent interface [ETW]","SetProviderId method","ITraceEvent.SetProviderId","ITraceEvent::SetProviderId","SetProviderId","SetProviderId method [ETW]","SetProviderId method [ETW]","ITraceEvent interface","etw.ievent_setproviderid","relogger/ITraceEvent::SetProviderId"]
old-location: etw\ievent_setproviderid.htm
tech.root: ETW
ms.assetid: dc61ff9e-2af9-4428-82df-84635313ddc6
ms.date: 12/05/2018
ms.keywords: ITraceEvent interface [ETW],SetProviderId method, ITraceEvent.SetProviderId, ITraceEvent::SetProviderId, SetProviderId, SetProviderId method [ETW], SetProviderId method [ETW],ITraceEvent interface, etw.ievent_setproviderid, relogger/ITraceEvent::SetProviderId
req.header: relogger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITraceEvent::SetProviderId
 - relogger/ITraceEvent::SetProviderId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceEvent.SetProviderId
---

# ITraceEvent::SetProviderId


## -description

The <b>SetProviderId</b> method sets the GUID for the provider which traced an event.

## -parameters

### -param ProviderId [in]

Type: <b>LPCGUID</b>

Unique identifier of the provider.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>