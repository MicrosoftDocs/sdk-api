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

# TERMINAL_TYPE enumeration


## -description


The 
<b>TERMINAL_TYPE</b> enum describes the type of the terminal. This enum is returned by the 
<a href="https://msdn.microsoft.com/b6f33151-2415-4f24-b84b-7f2ce724db5b">ITTerminal::get_TerminalType</a> method.


## -enum-fields




### -field TT_STATIC

A static terminal is a terminal that cannot be created and usually refers to hardware device. TAPI enumerates these terminals.


### -field TT_DYNAMIC

A terminal type that can be created. The application must call 
<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">ITTerminalSupport::CreateTerminal</a> to use this type of terminal.


## -see-also




<a href="https://msdn.microsoft.com/b6f33151-2415-4f24-b84b-7f2ce724db5b">ITTerminal::get_TerminalType</a>
 

 

