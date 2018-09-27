---
UID: NF:tapi3if.ITFileTerminalEvent.get_Terminal
title: ITFileTerminalEvent::get_Terminal
author: windows-sdk-content
description: The get_Terminal method returns the file terminal that generated this event.
old-location: tapi3\itfileterminalevent_get_terminal.htm
tech.root: tapi
ms.assetid: 515d9c65-1c24-485a-b7e4-1640e4e8c382
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Terminal method, ITFileTerminalEvent.get_Terminal, ITFileTerminalEvent::get_Terminal, _tapi3_itfileterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_terminal, tapi3if/ITFileTerminalEvent::get_Terminal
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
 - ITFileTerminalEvent.get_Terminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTerminalEvent::get_Terminal


## -description


The 
<b>get_Terminal</b> method returns the file terminal that generated this event.


## -parameters




### -param ppTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb6f2869-ec31-49ac-873b-35a0dcd2c8d7">ITFileTerminalEvent</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 

