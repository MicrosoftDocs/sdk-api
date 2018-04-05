---
UID: NE:tapi3if.TERMINAL_STATE
title: TERMINAL_STATE
author: windows-driver-content
description: The TERMINAL_STATE enum describes the current state of a terminal device. This enum is returned by the ITTerminal::get_State method.
old-location: tapi3\terminal_state.htm
old-project: Tapi
ms.assetid: 310c41f5-dfe7-491d-8669-87a98694f5b7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: TERMINAL_STATE, TERMINAL_STATE enumeration [TAPI 2.2], TS_INUSE, TS_NOTINUSE, _tapi3_terminal_state, tapi3.terminal_state, tapi3if/TERMINAL_STATE, tapi3if/TS_INUSE, tapi3if/TS_NOTINUSE
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TERMINAL_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi3if.h
api_name:
-	TERMINAL_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TERMINAL_STATE enumeration


## -description


The 
<b>TERMINAL_STATE</b> enum describes the current state of a terminal device. This enum is returned by the 
<a href="https://msdn.microsoft.com/18eebe2c-2c65-4836-a371-146eb76a379c">ITTerminal::get_State</a> method.


## -enum-fields




### -field TS_INUSE

The terminal is currently in use.


### -field TS_NOTINUSE

The terminal is not currently in use.


## -see-also




<a href="https://msdn.microsoft.com/18eebe2c-2c65-4836-a371-146eb76a379c">ITTerminal::get_State</a>
 

 

