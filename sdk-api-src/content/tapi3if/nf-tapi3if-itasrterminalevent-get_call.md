---
UID: NF:tapi3if.ITASRTerminalEvent.get_Call
title: ITASRTerminalEvent::get_Call
author: windows-sdk-content
description: The get_Call method returns a pointer to the ITCallInfo interface for the call object involved in the terminal event.
old-location: tapi3\itasrterminalevent_get_call.htm
old-project: tapi
ms.assetid: 8736e3bc-9f79-4b0f-84a7-00e6d20550e2
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITASRTerminalEvent interface [TAPI 2.2],get_Call method, ITASRTerminalEvent.get_Call, ITASRTerminalEvent::get_Call, _tapi3_itasrterminalevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITASRTerminalEvent interface, tapi3.itasrterminalevent_get_call, tapi3if/ITASRTerminalEvent::get_Call
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
 - ITASRTerminalEvent.get_Call
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITASRTerminalEvent::get_Call


## -description


The 
<b>get_Call</b> method returns a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface for the call object involved in the terminal event.


## -parameters




### -param ppCall [out]

Pointer to 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/6bf8b1b7-698f-443f-9ddf-0d50551cebab">ITASRTerminalEvent</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>
 

 

