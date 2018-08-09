---
UID: NC:webservices.WS_OPERATION_CANCEL_CALLBACK
title: WS_OPERATION_CANCEL_CALLBACK
author: windows-sdk-content
description: Gives notification of the cancellation of an asynchronous service operation call as a result of an aborted shutdown of service host.
old-location: wsw\ws_operation_cancel_callback.htm
old-project: wsw
ms.assetid: 177f9abb-861d-42a9-8044-25076b026f1d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_OPERATION_CANCEL_CALLBACK, WS_OPERATION_CANCEL_CALLBACK callback, WS_OPERATION_CANCEL_CALLBACK callback function [Web Services for Windows], webservices/WS_OPERATION_CANCEL_CALLBACK, wsw.ws_operation_cancel_callback
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_OPERATION_CANCEL_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_OPERATION_CANCEL_CALLBACK callback function


## -description


Gives notification of the cancellation of an 
                asynchronous service operation call as a result of an aborted shutdown of service host. 
             This callback is invoked by service model.


## -parameters




### -param reason [in]

Specifies the reason for which the call back is called.
                


### -param *state [in]

A reference to the application defined state registered with the callback. 
                


## -returns



This callback function does not return a value.




## -remarks



See <a href="https://msdn.microsoft.com/3e456814-f70f-47ab-b866-f0b73d5cd35e">WsRegisterOperationForCancel</a> for details.
            



