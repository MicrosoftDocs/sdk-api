---
UID: NC:webservices.WS_ASYNC_CALLBACK
title: WS_ASYNC_CALLBACK
author: windows-sdk-content
description: The callback function parameter used with the asynchronous model.
old-location: wsw\ws_async_callback.htm
tech.root: wsw
ms.assetid: 1322652f-ed9f-435f-b4ed-fa9ea425c5ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_ASYNC_CALLBACK, WS_ASYNC_CALLBACK callback, WS_ASYNC_CALLBACK callback function [Web Services for Windows], webservices/WS_ASYNC_CALLBACK, wsw.ws_async_callback
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WS_ASYNC_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_ASYNC_CALLBACK callback function


## -description


The callback function parameter used with the <a href="https://msdn.microsoft.com/d0b3f154-2219-4085-a652-e9aeb126598c">asynchronous model</a>.


## -parameters




### -param errorCode [in]

The result of the operation.   If the operation fails
                    and a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object is supplied, the object is filled with rich error information 
                    before the callback is invoked.
                


### -param callbackModel [in]

A <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">WS_CALLBACK_MODEL</a> value that determines whether the callback is being invoked as a long or short term callback.
                    


### -param *callbackState [in]

A void pointer that corresponds to the value of the <b>callbackState</b> field of 
                    the <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> structure. This parameter is used to pass user-defined data to the callback function if the operation completes asynchronously.


## -returns



This callback function does not return a value.




## -remarks



All error return codes of an operation are represented as HRESULTs. This API defines a set of HRESULTs in the FACILITY_WS range, but also returns errors defined elsewhere in the Windows API. 



