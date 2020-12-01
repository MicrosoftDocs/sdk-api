---
UID: NS:webservices._WS_DURATION_DESCRIPTION
title: WS_DURATION_DESCRIPTION (webservices.h)
description: An optional type description used with WS_DURATION_TYPE. It is used to specify constraints on the set of values which can be deserialized.
helpviewer_keywords: ["WS_DURATION_DESCRIPTION","WS_DURATION_DESCRIPTION structure [Web Services for Windows]","webservices/WS_DURATION_DESCRIPTION","wsw.ws_duration_description"]
old-location: wsw\ws_duration_description.htm
tech.root: wsw
ms.assetid: 51084a56-f666-4ca0-b98c-9f41e28b99c0
ms.date: 12/05/2018
ms.keywords: WS_DURATION_DESCRIPTION, WS_DURATION_DESCRIPTION structure [Web Services for Windows], webservices/WS_DURATION_DESCRIPTION, wsw.ws_duration_description
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
req.typenames: WS_DURATION_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_DURATION_DESCRIPTION
 - webservices/_WS_DURATION_DESCRIPTION
 - WS_DURATION_DESCRIPTION
 - webservices/WS_DURATION_DESCRIPTION
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
 - WS_DURATION_DESCRIPTION
---

# WS_DURATION_DESCRIPTION structure


## -description

An optional type description  used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_DURATION_TYPE</a>.
                It is used to specify constraints on the set of values
                which can be deserialized.

## -struct-fields

### -field minValue

The minimum value.

### -field maxValue

The maximum value.

### -field comparer

Specifies a function which can be used to compare <a href="/windows/desktop/api/webservices/ns-webservices-ws_duration">WS_DURATION</a>. If <b>NULL</b>, a default
                    comparer is used.
                

Because <a href="/windows/desktop/api/webservices/ns-webservices-ws_duration">WS_DURATION</a> has a partial ordering, not all durations can be unambiguously compared
                    (for example, 1 month and 30 days).  The default comparer function can compare durations that specify
                    years and months (but no other components), or durations that specify no years or months (but any other
                    component).