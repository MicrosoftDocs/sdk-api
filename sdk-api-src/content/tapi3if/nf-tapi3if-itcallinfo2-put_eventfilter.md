---
UID: NF:tapi3if.ITCallInfo2.put_EventFilter
title: ITCallInfo2::put_EventFilter
author: windows-sdk-content
description: The put_EventFilter method sets an event filter for the current call.
old-location: tapi3\itcallinfo2_put_eventfilter.htm
old-project: Tapi
ms.assetid: 8e1b4474-b9ff-489d-8226-58eda659e057
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITCallInfo2 interface [TAPI 2.2],put_EventFilter method, ITCallInfo2.put_EventFilter, ITCallInfo2::put_EventFilter, _tapi3_itcallinfo2_put_eventfilter, put_EventFilter, put_EventFilter method [TAPI 2.2], put_EventFilter method [TAPI 2.2],ITCallInfo2 interface, tapi3.itcallinfo2_put_eventfilter, tapi3if/ITCallInfo2::put_EventFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallInfo2.put_EventFilter
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallInfo2::put_EventFilter


## -description


The 
<b>put_EventFilter</b> method sets an event filter for the current call.


## -parameters




### -param TapiEvent [in]

The 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> descriptor of the event type.


### -param lSubEvent [in]

Subevent descriptor.


### -param bEnable [in]

VARIANT_TRUE if application requires notification of this event type. VARIANT_FALSE indicates the application does not require notifications for this event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/20f7b20e-37f8-49f7-ae9d-83a9b9f574b6">ITCallInfo2</a>
 

 

