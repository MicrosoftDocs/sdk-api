---
UID: NS:wsdtypes._WSD_HANDLER_CONTEXT
title: WSD_HANDLER_CONTEXT (wsdtypes.h)
author: windows-sdk-content
description: Specifies the context for handling incoming messages.
old-location: ncd\wsd_handler_context_struct.htm
tech.root: WsdApi
ms.assetid: d7b69627-5847-47ec-8ada-2df9b427e870
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_HANDLER_CONTEXT, WSD_HANDLER_CONTEXT structure, ncd.wsd_handler_context_struct, wsdtypes/WSD_HANDLER_CONTEXT
ms.topic: struct
f1_keywords: 
 - "wsdtypes/WSD_HANDLER_CONTEXT"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_HANDLER_CONTEXT
targetos: Windows
req.typenames: WSD_HANDLER_CONTEXT
req.redist: 
ms.custom: 19H1
---

# WSD_HANDLER_CONTEXT structure


## -description


Specifies the context for handling incoming messages.


## -struct-fields




### -field Handler


<a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/nc-wsdtypes-pwsd_soap_message_handler">PSWD_SOAP_MESSAGE_HANDLER</a> function that specifies the incoming message handler.


### -field PVoid

The value supplied by the <i>pVoidContext</i> parameter of the IWSDSession::AddPort, IWSDSession::RegisterForIncomingRequests, or IWSDSession::RegisterForIncomingResponse methods.


### -field Unknown

The value supplied by the <i>unknownContext</i> parameter of the IWSDSession::AddPort, IWSDSession::RegisterForIncomingRequests, or IWSDSession::RegisterForIncomingResponse methods.

