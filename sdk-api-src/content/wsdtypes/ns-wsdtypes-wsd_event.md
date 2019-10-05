---
UID: NS:wsdtypes._WSD_EVENT
title: WSD_EVENT (wsdtypes.h)
author: windows-sdk-content
description: Provides an internal representation of a SOAP message.
old-location: ncd\wsd_event_struct.htm
tech.root: WsdApi
ms.assetid: d8697474-bfe5-4704-b1ac-15cf96f2ca92
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_EVENT, WSD_EVENT structure, ncd.wsd_event_struct, wsdtypes/WSD_EVENT
ms.topic: struct
f1_keywords:
- wsdtypes/WSD_EVENT
dev_langs:
 - c++
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
- WSD_EVENT
targetos: Windows
req.typenames: WSD_EVENT
req.redist: 
ms.custom: 19H1
---

# WSD_EVENT structure


## -description


Provides an internal representation of a SOAP message.


## -struct-fields




### -field Hr

The result code of the event.


### -field EventType

The event type.


### -field DispatchTag

Pointer to the protocol string when dispatch by tags is required.


### -field HandlerContext

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_handler_context">WSD_HANDLER_CONTEXT</a> structure that specifies the handler context.


### -field Soap

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_message">WSD_SOAP_MESSAGE</a> structure that describes the event.


### -field Operation

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_operation">WSD_OPERATION</a> structure that specifies the operation performed.


### -field MessageParameters

Message transmission parameters.

