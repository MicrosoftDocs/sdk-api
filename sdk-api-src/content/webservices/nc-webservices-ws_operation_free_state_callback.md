---
UID: NC:webservices.WS_OPERATION_FREE_STATE_CALLBACK
title: WS_OPERATION_FREE_STATE_CALLBACK
author: windows-sdk-content
description: Allows an application to cleanup state information that was registered with cancellation callback.
old-location: wsw\ws_operation_free_state_callback.htm
tech.root: wsw
ms.assetid: 46b30bb3-00c6-4f54-b040-683cd6dd5525
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_OPERATION_FREE_STATE_CALLBACK, WS_OPERATION_FREE_STATE_CALLBACK callback, WS_OPERATION_FREE_STATE_CALLBACK callback function [Web Services for Windows], webservices/WS_OPERATION_FREE_STATE_CALLBACK, wsw.ws_operation_free_state_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_OPERATION_FREE_STATE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_OPERATION_FREE_STATE_CALLBACK callback function


## -description


Allows an application to cleanup 
                state information that was registered with cancellation callback. 
             
                This callback is invoked by service model.


## -parameters




### -param *state [in]

A reference to the application defined state registered with the callback. 
                


## -returns



This callback function does not return a value.




## -remarks



See <a href="https://msdn.microsoft.com/3e456814-f70f-47ab-b866-f0b73d5cd35e">WsRegisterOperationForCancel</a> for details.
            



