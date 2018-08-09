---
UID: NF:tapi3if.ITToneTerminalEvent.get_Call
title: ITToneTerminalEvent::get_Call
author: windows-sdk-content
description: The get_Call method retrieves an interface pointer for the call object on which the event occurred.
old-location: tapi3\ittoneterminalevent_get_call.htm
old-project: tapi
ms.assetid: adbbce76-827d-439c-865d-9dcfe40c9722
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITToneTerminalEvent interface [TAPI 2.2],get_Call method, ITToneTerminalEvent.get_Call, ITToneTerminalEvent::get_Call, _tapi3_ittoneterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITToneTerminalEvent interface, tapi3.ittoneterminalevent_get_call, tapi3if/ITToneTerminalEvent::get_Call
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
 - ITToneTerminalEvent.get_Call
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITToneTerminalEvent::get_Call


## -description


The 
<b>get_Call</b> method retrieves an interface pointer for the call object on which the event occurred.


## -parameters




### -param ppCall [out]

Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface returned by <b>ITToneTerminalEvent::get_Call</b>. The application must call <b>Release</b> on the 
<b>ITCallInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/6a5d03e9-e6d1-452a-a189-ca693a72c610">ITToneTerminalEvent</a>
 

 

