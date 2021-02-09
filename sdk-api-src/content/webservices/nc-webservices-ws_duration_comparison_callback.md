---
UID: NC:webservices.WS_DURATION_COMPARISON_CALLBACK
title: WS_DURATION_COMPARISON_CALLBACK (webservices.h)
description: Compares two durations.
helpviewer_keywords: ["WS_DURATION_COMPARISON_CALLBACK","WS_DURATION_COMPARISON_CALLBACK callback","WS_DURATION_COMPARISON_CALLBACK callback function [Web Services for Windows]","webservices/WS_DURATION_COMPARISON_CALLBACK","wsw.ws_duration_comparison_callback"]
old-location: wsw\ws_duration_comparison_callback.htm
tech.root: wsw
ms.assetid: 69f5d387-15b1-41cc-a0f8-047b8f6adb93
ms.date: 12/05/2018
ms.keywords: WS_DURATION_COMPARISON_CALLBACK, WS_DURATION_COMPARISON_CALLBACK callback, WS_DURATION_COMPARISON_CALLBACK callback function [Web Services for Windows], webservices/WS_DURATION_COMPARISON_CALLBACK, wsw.ws_duration_comparison_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_DURATION_COMPARISON_CALLBACK
 - webservices/WS_DURATION_COMPARISON_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_DURATION_COMPARISON_CALLBACK
---

# WS_DURATION_COMPARISON_CALLBACK callback function


## -description

Compares two durations.A duration represents a unit of time as an eight-dimensional space where the coordinates designate the year, month, day, hour, minute, second, millisecond, and CPU tick as represented by the <a href="/windows/desktop/api/webservices/ns-webservices-ws_duration">WS_DURATION</a> data structure.

## -parameters

### -param duration1 [in]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_duration">WS_DURATION</a> structure representing the first duration to compare.

### -param duration2 [in]

A  pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_duration">WS_DURATION</a> structure representing the second duration.

### -param result [out]

The relationship between the durations as one of the following values:
                    <ul>
<li>-1 if <i>duration1</i> is less than <i>duration2</i></li>
<li> 0 if <i>duration1</i> is equal to <i>duration2</i></li>
<li> 1 if <i>duration1</i> is greater than <i>duration2</i></li>
</ul>

### -param error [in, optional]

A pointer to  a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> handle where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.

## -remarks

If the function cannot compare the specified durations, it should return <b>WS_E_INVALID_FORMAT</b>. 
            (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)
