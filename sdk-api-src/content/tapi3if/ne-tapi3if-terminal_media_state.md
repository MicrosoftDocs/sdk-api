---
UID: NE:tapi3if.TERMINAL_MEDIA_STATE
title: TERMINAL_MEDIA_STATE
author: windows-sdk-content
description: The TERMINAL_MEDIA_STATE enum indicates the state of a file terminal.
old-location: tapi3\terminal_media_state.htm
tech.root: Tapi
ms.assetid: 9cc07684-9804-41ac-bc25-f37f6ae00280
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TERMINAL_MEDIA_STATE, TERMINAL_MEDIA_STATE enumeration [TAPI 2.2], TMS_ACTIVE, TMS_IDLE, TMS_LASTITEM, TMS_PAUSED, _tapi3_terminal_media_state, tapi3.terminal_media_state, tapi3if/TERMINAL_MEDIA_STATE, tapi3if/TMS_ACTIVE, tapi3if/TMS_IDLE, tapi3if/TMS_LASTITEM, tapi3if/TMS_PAUSED
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TERMINAL_MEDIA_STATE
product: Windows
targetos: Windows
req.typenames: TERMINAL_MEDIA_STATE
req.redist: 
---

# TERMINAL_MEDIA_STATE enumeration


## -description


The 
<b>TERMINAL_MEDIA_STATE</b> enum indicates the state of a file terminal.


## -enum-fields




### -field TMS_IDLE

The file terminal is idle.


### -field TMS_ACTIVE

The file terminal is active.


### -field TMS_PAUSED

The file terminal is paused.


### -field TMS_LASTITEM

Last item in this enum.


## -see-also




<a href="https://msdn.microsoft.com/f75537e8-f54c-4165-ba89-013eeabceb74">ITFileTerminalEvent::get_State</a>



<a href="https://msdn.microsoft.com/d28063cc-12fe-45b1-8f6a-8c2436926e12">ITMediaControl::get_MediaState</a>
 

 

