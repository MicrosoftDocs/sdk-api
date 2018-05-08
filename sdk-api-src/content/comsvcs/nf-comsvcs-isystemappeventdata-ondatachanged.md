---
UID: NF:comsvcs.ISystemAppEventData.OnDataChanged
title: ISystemAppEventData::OnDataChanged
author: windows-driver-content
description: Generated when the configuration of a COM+ application instance is changed.
old-location: cos\isystemappeventdata_ondatachanged.htm
old-project: cossdk
ms.assetid: db30c40e-8dd8-4055-b2c4-71f9d0c2efc4
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ISystemAppEventData interface [COM+],OnDataChanged method, ISystemAppEventData.OnDataChanged, ISystemAppEventData::OnDataChanged, OnDataChanged, OnDataChanged method [COM+], OnDataChanged method [COM+],ISystemAppEventData interface, _dtc_ISystemAppEventData_OnDataChanged, comsvcs/ISystemAppEventData::OnDataChanged, cos.isystemappeventdata_ondatachanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ISystemAppEventData.OnDataChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fd88641e-e0ce-44b7-b8b6-59791be48026">ISystemAppEventData</a>
 

 

