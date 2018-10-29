---
UID: NF:tapi3if.ITASRTerminalEvent.get_Terminal
title: ITASRTerminalEvent::get_Terminal
author: windows-sdk-content
description: The get_Terminal method returns a pointer to the ITTerminal interface for the terminal on which the event occurred.
old-location: tapi3\itasrterminalevent_get_terminal.htm
tech.root: Tapi
ms.assetid: 1cde7b16-f825-4591-9947-6ad03cbd14c6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITASRTerminalEvent interface [TAPI 2.2],get_Terminal method, ITASRTerminalEvent.get_Terminal, ITASRTerminalEvent::get_Terminal, _tapi3_itasrterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITASRTerminalEvent interface, tapi3.itasrterminalevent_get_terminal, tapi3if/ITASRTerminalEvent::get_Terminal
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
 - ITASRTerminalEvent.get_Terminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITASRTerminalEvent::get_Terminal


## -description


The 
<b>get_Terminal</b> method returns a pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface for the terminal on which the event occurred.


## -parameters




### -param ppTerminal [out]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/6bf8b1b7-698f-443f-9ddf-0d50551cebab">ITASRTerminalEvent</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 

