---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

