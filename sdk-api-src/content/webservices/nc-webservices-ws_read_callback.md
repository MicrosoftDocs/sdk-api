---
UID: NC:webservices.WS_READ_CALLBACK
title: WS_READ_CALLBACK (webservices.h)
description: Used by the WS_XML_READERto read from some source into a buffer.
helpviewer_keywords: ["WS_READ_CALLBACK","WS_READ_CALLBACK callback","WS_READ_CALLBACK callback function [Web Services for Windows]","webservices/WS_READ_CALLBACK","wsw.ws_read_callback"]
old-location: wsw\ws_read_callback.htm
tech.root: wsw
ms.assetid: 2a5ebe4a-e97d-4744-9ec9-da6da892e4c5
ms.date: 12/05/2018
ms.keywords: WS_READ_CALLBACK, WS_READ_CALLBACK callback, WS_READ_CALLBACK callback function [Web Services for Windows], webservices/WS_READ_CALLBACK, wsw.ws_read_callback
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
 - WS_READ_CALLBACK
 - webservices/WS_READ_CALLBACK
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
 - WS_READ_CALLBACK
---

# WS_READ_CALLBACK callback function


## -description

Used by the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> to read from some source into a buffer.

## -parameters

### -param callbackState [in]

A   <b>void</b> pointer to the user-defined state value that was passed to the function that accepted this callback.

### -param bytes

A <b>void</b> pointer to the location where the data should be placed.

### -param maxSize [in]

The maximum number of bytes that may be read.

### -param actualSize [out]

A pointer to a <b>ULONG</b>  value that indicates the number of bytes actually read.  This may be less than maxSize.  Returning 0
          indicates that there is no more data.

### -param asyncContext [in, optional]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> structure containing information on how to invoke the function asynchronously.  Assigned <b>NULL</b> if invoking synchronously.

### -param error [in, optional]

A pointer to <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> data structure where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.

## -remarks

Returning size of 0 in the <i>actualSize</i> output parameter indicates the end of the file.
