---
UID: NF:tapi3if.ITFileTerminalEvent.get_State
title: ITFileTerminalEvent::get_State (tapi3if.h)
author: windows-sdk-content
description: The get_State method gets information on the new file terminal state.
old-location: tapi3\itfileterminalevent_get_state.htm
tech.root: Tapi
ms.assetid: f75537e8-f54c-4165-ba89-013eeabceb74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_State method, ITFileTerminalEvent.get_State, ITFileTerminalEvent::get_State, _tapi3_itfileterminalevent_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_state, tapi3if/ITFileTerminalEvent::get_State
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
 - ITFileTerminalEvent.get_State
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITFileTerminalEvent::get_State


## -description


The 
<b>get_State</b> method gets information on the new file terminal state.


## -parameters




### -param pState [out]


<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-terminal_media_state">TERMINAL_MEDIA_STATE</a> descriptor of the new terminal state.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent">ITFileTerminalEvent</a>
 

 

