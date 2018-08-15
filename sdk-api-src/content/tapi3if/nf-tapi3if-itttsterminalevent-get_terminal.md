---
UID: NF:tapi3if.ITTTSTerminalEvent.get_Terminal
title: ITTTSTerminalEvent::get_Terminal
author: windows-sdk-content
description: The get_Terminal method gets an ITTerminal interface pointer for the terminal object involved in the event.
old-location: tapi3\itttsterminalevent_get_terminal.htm
old-project: tapi
ms.assetid: ce37e074-8ce0-4fde-b16a-c85a9487f0db
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITTTSTerminalEvent interface [TAPI 2.2],get_Terminal method, ITTTSTerminalEvent.get_Terminal, ITTTSTerminalEvent::get_Terminal, _tapi3_itttsterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITTTSTerminalEvent interface, tapi3.itttsterminalevent_get_terminal, tapi3if/ITTTSTerminalEvent::get_Terminal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
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
 - ITTTSTerminalEvent.get_Terminal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTTSTerminalEvent::get_Terminal


## -description


The 
<b>get_Terminal</b> method gets an 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface pointer for the terminal object involved in the event.


## -parameters




### -param ppTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITTTSTerminalEvent::get_Terminal</b>. The application must call <b>Release</b> on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/0375d6e4-cd9f-4245-abf5-1b200af79848">ITTTSTerminalEvent</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 

