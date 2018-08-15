---
UID: NS:wsdtypes._WSD_HANDLER_CONTEXT
title: "_WSD_HANDLER_CONTEXT"
author: windows-sdk-content
description: Specifies the context for handling incoming messages.
old-location: ncd\wsd_handler_context_struct.htm
old-project: wsdapi
ms.assetid: d7b69627-5847-47ec-8ada-2df9b427e870
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_HANDLER_CONTEXT, WSD_HANDLER_CONTEXT structure, _WSD_HANDLER_CONTEXT, ncd.wsd_handler_context_struct, wsdtypes/WSD_HANDLER_CONTEXT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.redist: 
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
tech.root: 
req.typenames: WSD_HANDLER_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_HANDLER_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_HANDLER_CONTEXT structure


## -description


Specifies the context for handling incoming messages.


## -struct-fields




### -field Handler


<a href="https://msdn.microsoft.com/175d4352-ba85-4c3c-be9f-4612c4b66123">PSWD_SOAP_MESSAGE_HANDLER</a> function that specifies the incoming message handler.


### -field PVoid

The value supplied by the <i>pVoidContext</i> parameter of the IWSDSession::AddPort, IWSDSession::RegisterForIncomingRequests, or IWSDSession::RegisterForIncomingResponse methods.


### -field Unknown

The value supplied by the <i>unknownContext</i> parameter of the IWSDSession::AddPort, IWSDSession::RegisterForIncomingRequests, or IWSDSession::RegisterForIncomingResponse methods.

