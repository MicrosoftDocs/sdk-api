---
UID: NC:webservices.WS_WRITE_CALLBACK
title: WS_WRITE_CALLBACK (webservices.h)
description: Used by the WS_XML_WRITER function to write a specified buffer to a user-determined destination.
old-location: wsw\ws_write_callback.htm
tech.root: wsw
ms.assetid: 8d106ac2-226d-4e0c-8f14-8d3e17f15548
ms.date: 12/05/2018
ms.keywords: WS_WRITE_CALLBACK, WS_WRITE_CALLBACK callback, WS_WRITE_CALLBACK callback function [Web Services for Windows], webservices/WS_WRITE_CALLBACK, wsw.ws_write_callback
ms.topic: callback
f1_keywords:
- webservices/WS_WRITE_CALLBACK
dev_langs:
- c++
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
- UserDefined
api_location:
- WebServices.h
api_name:
- WS_WRITE_CALLBACK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WS_WRITE_CALLBACK callback function


## -description


Used by the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> function
        to write a specified buffer to a user-determined destination.


## -parameters




### -param *callbackState [in]

A   <b>void</b> pointer to the user-defined state value that was passed to the function that accepted this callback. 


### -param *buffers

A  pointer to the buffers containing the data to be written.
        


### -param count [in]

The number of buffers to write.
        


### -param *asyncContext [in, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> structure containing information on how to invoke the function asynchronously.  Assigned <b>NULL</b> if invoking synchronously.


### -param *error [in, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-error">WS_ERROR</a> data structure where additional error information should be stored if the function fails.
        


## -returns



This callback function does not return a value.



