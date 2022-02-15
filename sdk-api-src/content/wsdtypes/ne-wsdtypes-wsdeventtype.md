---
UID: NE:wsdtypes._WSDEventType
title: WSDEventType (wsdtypes.h)
description: Identifies the type of event produced by the session layer.
helpviewer_keywords: ["WSDET_INCOMING_FAULT","WSDET_INCOMING_MESSAGE","WSDET_NONE","WSDET_RESPONSE_TIMEOUT","WSDET_TRANSMISSION_FAILURE","WSDEventType","WSDEventType enumeration","ncd.wsdeventtype_enum","wsdtypes/WSDET_INCOMING_FAULT","wsdtypes/WSDET_INCOMING_MESSAGE","wsdtypes/WSDET_NONE","wsdtypes/WSDET_RESPONSE_TIMEOUT","wsdtypes/WSDET_TRANSMISSION_FAILURE","wsdtypes/WSDEventType"]
old-location: ncd\wsdeventtype_enum.htm
tech.root: ncd
ms.assetid: e65742da-57ef-44a8-be3b-5736714747d3
ms.date: 12/05/2018
ms.keywords: WSDET_INCOMING_FAULT, WSDET_INCOMING_MESSAGE, WSDET_NONE, WSDET_RESPONSE_TIMEOUT, WSDET_TRANSMISSION_FAILURE, WSDEventType, WSDEventType enumeration, ncd.wsdeventtype_enum, wsdtypes/WSDET_INCOMING_FAULT, wsdtypes/WSDET_INCOMING_MESSAGE, wsdtypes/WSDET_NONE, wsdtypes/WSDET_RESPONSE_TIMEOUT, wsdtypes/WSDET_TRANSMISSION_FAILURE, wsdtypes/WSDEventType
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
req.typenames: WSDEventType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSDEventType
 - wsdtypes/_WSDEventType
 - WSDEventType
 - wsdtypes/WSDEventType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsdtypes.h
api_name:
 - WSDEventType
---

# WSDEventType enumeration


## -description

Identifies the type of event produced by the session layer.

## -enum-fields

### -field WSDET_NONE:0

No events were detected.

### -field WSDET_INCOMING_MESSAGE:1

An incoming message was detected.

### -field WSDET_INCOMING_FAULT:2

An incoming message fault was detected.

### -field WSDET_TRANSMISSION_FAILURE:3

A message transmission failure was detected.

### -field WSDET_RESPONSE_TIMEOUT:4

A message response timeout was detected.

