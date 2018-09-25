---
UID: NF:tapi3if.ITTTSTerminalEvent.get_Call
title: ITTTSTerminalEvent::get_Call
author: windows-sdk-content
description: The get_Call method returns an ITCallInfo interface pointer for the call involved in the terminal event.
old-location: tapi3\itttsterminalevent_get_call.htm
tech.root: tapi
ms.assetid: 7e9ffff3-1282-4d05-83c9-7f824406fcfa
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITTTSTerminalEvent interface [TAPI 2.2],get_Call method, ITTTSTerminalEvent.get_Call, ITTTSTerminalEvent::get_Call, _tapi3_itttsterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITTTSTerminalEvent interface, tapi3.itttsterminalevent_get_call, tapi3if/ITTTSTerminalEvent::get_Call
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
 - ITTTSTerminalEvent.get_Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTTSTerminalEvent::get_Call


## -description


The 
<b>get_Call</b> method returns an 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface pointer for the call involved in the terminal event.


## -parameters




### -param ppCall [out]

Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface returned by <b>ITTTSTerminalEvent::get_Call</b>. The application must call <b>Release</b> on the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/0375d6e4-cd9f-4245-abf5-1b200af79848">ITTTSTerminalEvent</a>
 

 

