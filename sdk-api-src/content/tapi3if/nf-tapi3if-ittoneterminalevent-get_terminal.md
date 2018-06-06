---
UID: NF:tapi3if.ITToneTerminalEvent.get_Terminal
title: ITToneTerminalEvent::get_Terminal
author: windows-sdk-content
description: The get_Terminal method returns an ITTerminal pointer for the tone terminal on which the event occurred.
old-location: tapi3\ittoneterminalevent_get_terminal.htm
old-project: Tapi
ms.assetid: 3358e219-fde9-4b60-bf75-c6d8c42a51ea
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITToneTerminalEvent interface [TAPI 2.2],get_Terminal method, ITToneTerminalEvent.get_Terminal, ITToneTerminalEvent::get_Terminal, _tapi3_ittoneterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITToneTerminalEvent interface, tapi3.ittoneterminalevent_get_terminal, tapi3if/ITToneTerminalEvent::get_Terminal
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
 - ITToneTerminalEvent.get_Terminal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITToneTerminalEvent::get_Terminal


## -description


The 
<b>get_Terminal</b> method returns an 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> pointer for the tone terminal on which the event occurred.


## -parameters




### -param ppTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITToneTerminalEvent::get_Terminal</b>. The application must call <b>Release</b> on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/6a5d03e9-e6d1-452a-a189-ca693a72c610">ITToneTerminalEvent</a>
 

 

