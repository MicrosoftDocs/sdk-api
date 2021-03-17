---
UID: NS:webservices._WS_DURATION
title: WS_DURATION (webservices.h)
description: Represents a xsd:duration data type.
helpviewer_keywords: ["WS_DURATION","WS_DURATION structure [Web Services for Windows]","webservices/WS_DURATION","wsw.ws_duration"]
old-location: wsw\ws_duration.htm
tech.root: wsw
ms.assetid: ccb08c23-8c6f-4ea7-a43b-c30a0df75805
ms.date: 12/05/2018
ms.keywords: WS_DURATION, WS_DURATION structure [Web Services for Windows], webservices/WS_DURATION, wsw.ws_duration
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_DURATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_DURATION
 - webservices/_WS_DURATION
 - WS_DURATION
 - webservices/WS_DURATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_DURATION
---

# WS_DURATION structure


## -description

Represents a <a href="https://www.w3.org/TR/xmlschema-2/#duration">xsd:duration</a> data type.

## -struct-fields

### -field negative

If <b>TRUE</b>, this represents a negative duration.

### -field years

The number of years.

### -field months

The number of months.

### -field days

The number of days.

### -field hours

The number of hours.

### -field minutes

The number of minutes.

### -field seconds

The number of seconds.

### -field milliseconds

The number of milliseconds.  This value must be less than 1000.

### -field ticks

Indicates the number of ticks.  This value must be less than 10000.

