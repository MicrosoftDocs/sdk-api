---
UID: NS:wsdtypes._WSD_EVENT
title: "_WSD_EVENT"
author: windows-sdk-content
description: Provides an internal representation of a SOAP message.
old-location: ncd\wsd_event_struct.htm
tech.root: WsdApi
ms.assetid: d8697474-bfe5-4704-b1ac-15cf96f2ca92
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSD_EVENT, WSD_EVENT structure, _WSD_EVENT, ncd.wsd_event_struct, wsdtypes/WSD_EVENT
ms.prod: windows
ms.technology: windows-sdk
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
product: Windows
targetos: Windows
req.typenames: WSD_EVENT
req.redist: 
---

# _WSD_EVENT structure


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

Reference to a <a href="https://msdn.microsoft.com/d7b69627-5847-47ec-8ada-2df9b427e870">WSD_HANDLER_CONTEXT</a> structure that specifies the handler context.


### -field Soap

Reference to a <a href="https://msdn.microsoft.com/e5352a78-3ece-45d3-bf95-2d922065e3d5">WSD_SOAP_MESSAGE</a> structure that describes the event.


### -field Operation

Reference to a <a href="https://msdn.microsoft.com/fcd4895d-5357-4b73-90b9-e506e3d7f16e">WSD_OPERATION</a> structure that specifies the operation performed.


### -field MessageParameters

Message transmission parameters.

