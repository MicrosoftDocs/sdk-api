---
UID: NF:tapi3if.ITFileTerminalEvent.get_Call
title: ITFileTerminalEvent::get_Call
author: windows-sdk-content
description: The get_Call method gets a pointer to the call information interface for the call on which the event has occurred.
old-location: tapi3\itfileterminalevent_get_call.htm
tech.root: tapi
ms.assetid: 4a9745a7-8119-41a0-b09a-3475f2390d4d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Call method, ITFileTerminalEvent.get_Call, ITFileTerminalEvent::get_Call, _tapi3_itfileterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_call, tapi3if/ITFileTerminalEvent::get_Call
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
 - ITFileTerminalEvent.get_Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTerminalEvent::get_Call


## -description


The 
<b>get_Call</b> method gets a pointer to the call information interface for the call on which the event has occurred.


## -parameters




### -param ppCall [out]

Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a terminal must generate an event, it requires a selected track in order to pass the event to an MSP which will then pass it to the application through TAPI. The first track that accepts the task of sending the event will be used. If the terminal has more than one track and the tracks are selected onto streams that belong to different calls, the call object pointer eventually returned could be for any of those calls.




## -see-also




<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/cb6f2869-ec31-49ac-873b-35a0dcd2c8d7">ITFileTerminalEvent</a>
 

 

