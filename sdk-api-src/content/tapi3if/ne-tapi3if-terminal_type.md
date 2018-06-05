---
UID: NE:tapi3if.TERMINAL_TYPE
title: TERMINAL_TYPE
author: windows-sdk-content
description: The TERMINAL_TYPE enum describes the type of the terminal. This enum is returned by the ITTerminal::get_TerminalType method.
old-location: tapi3\terminal_type.htm
old-project: Tapi
ms.assetid: 43d08be3-c09b-4c74-ad71-6b452850d2e0
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: TERMINAL_TYPE, TERMINAL_TYPE enumeration [TAPI 2.2], TT_DYNAMIC, TT_STATIC, _tapi3_terminal_type, tapi3.terminal_type, tapi3if/TERMINAL_TYPE, tapi3if/TT_DYNAMIC, tapi3if/TT_STATIC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi3if.h
api_name:
-	TERMINAL_TYPE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

