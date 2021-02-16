---
UID: NS:wsdtypes._WSD_SYNCHRONOUS_RESPONSE_CONTEXT
title: WSD_SYNCHRONOUS_RESPONSE_CONTEXT (wsdtypes.h)
description: Provides a context for handling the response to a two-way request.
helpviewer_keywords: ["WSD_SYNCHRONOUS_RESPONSE_CONTEXT","WSD_SYNCHRONOUS_RESPONSE_CONTEXT structure","ncd.wsd_synchronous_response_context_struct","wsdtypes/WSD_SYNCHRONOUS_RESPONSE_CONTEXT"]
old-location: ncd\wsd_synchronous_response_context_struct.htm
tech.root: ncd
ms.assetid: 591cf076-f55f-4e78-aa5e-94ea8db3d102
ms.date: 12/05/2018
ms.keywords: WSD_SYNCHRONOUS_RESPONSE_CONTEXT, WSD_SYNCHRONOUS_RESPONSE_CONTEXT structure, ncd.wsd_synchronous_response_context_struct, wsdtypes/WSD_SYNCHRONOUS_RESPONSE_CONTEXT
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSD_SYNCHRONOUS_RESPONSE_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_SYNCHRONOUS_RESPONSE_CONTEXT
 - wsdtypes/_WSD_SYNCHRONOUS_RESPONSE_CONTEXT
 - WSD_SYNCHRONOUS_RESPONSE_CONTEXT
 - wsdtypes/WSD_SYNCHRONOUS_RESPONSE_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_SYNCHRONOUS_RESPONSE_CONTEXT
---

# WSD_SYNCHRONOUS_RESPONSE_CONTEXT structure


## -description

Provides a context for handling the response to a two-way request.

## -struct-fields

### -field hr

The result code of the last operation performed using this response context.

### -field eventHandle

The event handle to be signaled when the response is ready.

### -field messageParameters

A pointer to an <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a> object that contains transport information associated with the response.

### -field results

The body of the response message.