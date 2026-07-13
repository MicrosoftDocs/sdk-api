---
UID: NF:comsvcs.ISystemAppEventData.OnDataChanged
title: ISystemAppEventData::OnDataChanged (comsvcs.h)
description: Generated when the configuration of a COM+ application instance is changed.
helpviewer_keywords: ["ISystemAppEventData interface [COM+]","OnDataChanged method","ISystemAppEventData.OnDataChanged","ISystemAppEventData::OnDataChanged","OnDataChanged","OnDataChanged method [COM+]","OnDataChanged method [COM+]","ISystemAppEventData interface","_dtc_ISystemAppEventData_OnDataChanged","comsvcs/ISystemAppEventData::OnDataChanged","cos.isystemappeventdata_ondatachanged"]
old-location: cos\isystemappeventdata_ondatachanged.htm
tech.root: cos
ms.assetid: db30c40e-8dd8-4055-b2c4-71f9d0c2efc4
ms.date: 12/05/2018
ms.keywords: ISystemAppEventData interface [COM+],OnDataChanged method, ISystemAppEventData.OnDataChanged, ISystemAppEventData::OnDataChanged, OnDataChanged, OnDataChanged method [COM+], OnDataChanged method [COM+],ISystemAppEventData interface, _dtc_ISystemAppEventData_OnDataChanged, comsvcs/ISystemAppEventData::OnDataChanged, cos.isystemappeventdata_ondatachanged
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISystemAppEventData::OnDataChanged
 - comsvcs/ISystemAppEventData::OnDataChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISystemAppEventData.OnDataChanged
---

# ISystemAppEventData::OnDataChanged


## -description

Generated when the configuration of a COM+ application instance is changed.

## -parameters

### -param dwPID [in]

The process identifier of the application instance for which the configuration was changed.

### -param dwMask [in]

The event mask used to determine which tracing event fires.

### -param dwNumberSinks [in]

Always set equal to SinkType::NUMBER_SINKS.

### -param bstrDwMethodMask [in]

The event mask used to determine to which events the user has subscribed.

### -param dwReason [in]

Always set equal to INFO_MASKCHANGED.

### -param u64TraceHandle [in]

A handle to the relevant tracing session.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isystemappeventdata">ISystemAppEventData</a>