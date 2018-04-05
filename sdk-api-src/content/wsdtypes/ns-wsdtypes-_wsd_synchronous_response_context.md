---
UID: NS:wsdtypes._WSD_SYNCHRONOUS_RESPONSE_CONTEXT
title: "_WSD_SYNCHRONOUS_RESPONSE_CONTEXT"
author: windows-driver-content
description: Provides a context for handling the response to a two-way request.
old-location: ncd\wsd_synchronous_response_context_struct.htm
old-project: WsdApi
ms.assetid: 591cf076-f55f-4e78-aa5e-94ea8db3d102
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSD_SYNCHRONOUS_RESPONSE_CONTEXT, WSD_SYNCHRONOUS_RESPONSE_CONTEXT structure, _WSD_SYNCHRONOUS_RESPONSE_CONTEXT, ncd.wsd_synchronous_response_context_struct, wsdtypes/WSD_SYNCHRONOUS_RESPONSE_CONTEXT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_SYNCHRONOUS_RESPONSE_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_SYNCHRONOUS_RESPONSE_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_SYNCHRONOUS_RESPONSE_CONTEXT structure


## -description


Provides a context for handling the response to a two-way request.




## -struct-fields




### -field hr

The result code of the last operation performed using this response context.


### -field eventHandle

The event handle to be signaled when the response is ready.


### -field messageParameters

A pointer to an <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> object that contains transport information associated with the response. 



### -field results

The body of the response message.

