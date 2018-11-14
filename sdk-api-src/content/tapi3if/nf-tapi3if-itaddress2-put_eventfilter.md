---
UID: NF:tapi3if.ITAddress2.put_EventFilter
title: ITAddress2::put_EventFilter
author: windows-sdk-content
description: The put_EventFilter method sets an event filter for the current address. If no event filters are set, the application will not be notified of events on this address.
old-location: tapi3\itaddress2_put_eventfilter.htm
tech.root: tapi
ms.assetid: ca58c796-d843-48c3-9eac-ca126395d448
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAddress2 interface [TAPI 2.2],put_EventFilter method, ITAddress2.put_EventFilter, ITAddress2::put_EventFilter, _tapi3_itaddress2_put_eventfilter, put_EventFilter, put_EventFilter method [TAPI 2.2], put_EventFilter method [TAPI 2.2],ITAddress2 interface, tapi3.itaddress2_put_eventfilter, tapi3if/ITAddress2::put_EventFilter
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress2.put_EventFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITAddress2.put_EventFilter
: 
---

# ITAddress2::put_EventFilter


## -description


The 
<b>put_EventFilter</b> method sets an event filter for the current address. If no event filters are set, the application will not be notified of events on this address.


## -parameters




### -param TapiEvent [in]

The 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> descriptor of the event type.


### -param lSubEvent [in]

Subevent descriptor.


### -param bEnable [in]

VARIANT_TRUE if the application requires notification of this event type. VARIANT_FALSE if the application does not require notifications for this event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

