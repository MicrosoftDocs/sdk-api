---
UID: NF:tapi3if.ITFileTerminalEvent.get_Cause
title: ITFileTerminalEvent::get_Cause
author: windows-sdk-content
description: The get_Cause method gets the cause associated with this event.
old-location: tapi3\itfileterminalevent_get_cause.htm
tech.root: TAPI
ms.assetid: 90594778-712e-4d26-9fe5-cb5cfd240359
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Cause method, ITFileTerminalEvent.get_Cause, ITFileTerminalEvent::get_Cause, _tapi3_itfileterminalevent_get_cause, get_Cause, get_Cause method [TAPI 2.2], get_Cause method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_cause, tapi3if/ITFileTerminalEvent::get_Cause
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
 - ITFileTerminalEvent.get_Cause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTerminalEvent::get_Cause


## -description


The 
<b>get_Cause</b> method gets the cause associated with this event.


## -parameters




### -param pCause [out]


<a href="https://msdn.microsoft.com/dd81fe2d-07ab-404b-8510-52029d67ef9b">FT_STATE_EVENT_CAUSE</a> descriptor of the cause of this event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb6f2869-ec31-49ac-873b-35a0dcd2c8d7">ITFileTerminalEvent</a>
 

 

