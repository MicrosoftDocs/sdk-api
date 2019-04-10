---
UID: NF:tapi3if.ITAddress2.get_EventFilter
title: ITAddress2::get_EventFilter (tapi3if.h)
author: windows-sdk-content
description: The get_EventFilter method retrieves the current filter settings for the current address and a given TAPI_EVENT value.
old-location: tapi3\itaddress2_get_eventfilter.htm
tech.root: Tapi
ms.assetid: cb0fbfc1-56bf-4455-8d6a-71c78b6a6534
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAddress2 interface [TAPI 2.2],get_EventFilter method, ITAddress2.get_EventFilter, ITAddress2::get_EventFilter, _tapi3_itaddress2_get_eventfilter, get_EventFilter, get_EventFilter method [TAPI 2.2], get_EventFilter method [TAPI 2.2],ITAddress2 interface, tapi3.itaddress2_get_eventfilter, tapi3if/ITAddress2::get_EventFilter
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
 - ITAddress2.get_EventFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress2::get_EventFilter


## -description


The 
<b>get_EventFilter</b> method retrieves the current filter settings for the current address and a given 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> value.

If no filters are set for an address, no event information for that address will be sent to the application.


## -parameters




### -param TapiEvent [in]

The 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> descriptor of event type information being checked.


### -param lSubEvent [in]

Subevent value. <b>NULL</b> if not applicable.


### -param pEnable [out]

Pointer to VARIANT_BOOL indicating whether the current event is required by the application.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>
 

 

