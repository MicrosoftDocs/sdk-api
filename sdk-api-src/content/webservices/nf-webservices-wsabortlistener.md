---
UID: NF:webservices.WsAbortListener
title: WsAbortListener function
author: windows-sdk-content
description: Cancels any pending I/O for the specified listener.
old-location: wsw\wsabortlistener.htm
old-project: wsw
ms.assetid: 894a325b-53ac-4f45-ac24-87ed3a40b03d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsAbortListener, WsAbortListener function [Web Services for Windows], webservices/WsAbortListener, wsw.wsabortlistener
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsAbortListener
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAbortListener function


## -description



Cancels any pending I/O for the specified <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">listener</a>.




## -parameters




### -param listener [in]

Pointer to a <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> structure representing the listener for which to cancel I/O.
                


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.




## -remarks



<b>WsAbortListener</b> can be called when the listener is in any state. (See the <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a> enumeration for possible states.) If the listener is in the WS_LISTENER_STATE_OPEN state,  this function will force the listener to fault (reset to the WS_LISTENER_STATE_FAULTED state). When a listener is faulted, all attempts to accept a message from it fail immediately with the WS_E_OBJECT_FAULTED error code. 



This function does not wait for pending I/O to complete.
            

If called with valid parameters, this function will not fail for reasons such as a lack of system resources.



