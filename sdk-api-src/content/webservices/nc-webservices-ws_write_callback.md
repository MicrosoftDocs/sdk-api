---
UID: NC:webservices.WS_WRITE_CALLBACK
title: WS_WRITE_CALLBACK
author: windows-sdk-content
description: Used by the WS_XML_WRITER function to write a specified buffer to a user-determined destination.
old-location: wsw\ws_write_callback.htm
tech.root: wsw
ms.assetid: 8d106ac2-226d-4e0c-8f14-8d3e17f15548
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_WRITE_CALLBACK, WS_WRITE_CALLBACK callback, WS_WRITE_CALLBACK callback function [Web Services for Windows], webservices/WS_WRITE_CALLBACK, wsw.ws_write_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_WRITE_CALLBACK callback function


## -description


Used by the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> function
        to write a specified buffer to a user-determined destination.


## -parameters




### -param *callbackState [in]

A   <b>void</b> pointer to the user-defined state value that was passed to the function that accepted this callback. 


### -param *buffers

A  pointer to the buffers containing the data to be written.
        


### -param count [in]

The number of buffers to write.
        


### -param *asyncContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> structure containing information on how to invoke the function asynchronously.  Assigned <b>NULL</b> if invoking synchronously.


### -param *error [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> data structure where additional error information should be stored if the function fails.
        


## -returns



This callback function does not return a value.



