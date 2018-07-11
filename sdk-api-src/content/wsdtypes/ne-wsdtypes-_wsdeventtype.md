---
UID: NE:wsdtypes._WSDEventType
title: "_WSDEventType"
author: windows-sdk-content
description: Identifies the type of event produced by the session layer.
old-location: ncd\wsdeventtype_enum.htm
old-project: wsdapi
ms.assetid: e65742da-57ef-44a8-be3b-5736714747d3
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: WSDET_INCOMING_FAULT, WSDET_INCOMING_MESSAGE, WSDET_NONE, WSDET_RESPONSE_TIMEOUT, WSDET_TRANSMISSION_FAILURE, WSDEventType, WSDEventType enumeration, _WSDEventType, ncd.wsdeventtype_enum, wsdtypes/WSDET_INCOMING_FAULT, wsdtypes/WSDET_INCOMING_MESSAGE, wsdtypes/WSDET_NONE, wsdtypes/WSDET_RESPONSE_TIMEOUT, wsdtypes/WSDET_TRANSMISSION_FAILURE, wsdtypes/WSDEventType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WSDEventType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsdtypes.h
api_name:
 - WSDEventType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSDEventType enumeration


## -description


Identifies the type of event produced by the session layer.


## -enum-fields




### -field WSDET_NONE

No events were detected.


### -field WSDET_INCOMING_MESSAGE

An incoming message was detected.


### -field WSDET_INCOMING_FAULT

An incoming message fault was detected.


### -field WSDET_TRANSMISSION_FAILURE

A message transmission failure was detected.


### -field WSDET_RESPONSE_TIMEOUT

A message response timeout was detected.

