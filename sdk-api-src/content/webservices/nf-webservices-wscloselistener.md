---
UID: NF:webservices.WsCloseListener
title: WsCloseListener function
author: windows-sdk-content
description: Causes the specified listener to stop listening.
old-location: wsw\wscloselistener.htm
old-project: wsw
ms.assetid: 6023595a-ac52-4619-a824-df49da887fc5
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsCloseListener, WsCloseListener function [Web Services for Windows], webservices/WsCloseListener, wsw.wscloselistener
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
 - WsCloseListener
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCloseListener function


## -description



Causes the specified <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">listener</a>  to stop listening.
            




## -parameters




### -param listener [in]

Pointer to a <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> structure representing the listener  to close.
                


### -param asyncContext [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> structure containing information for invoking the function asynchronously. Pass <b>NULL</b> to invoke the function synchronously.


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">

                    The asynchronous operation is still pending.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">

                    The close was aborted by a call to <a href="https://msdn.microsoft.com/894a325b-53ac-4f45-ac24-87ed3a40b03d">WsAbortListener</a> as the listener was closing.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

                    The listener was in an inappropriate state.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_TIMED_OUT</b></dt>
</dl>
</td>
<td width="60%">

The operation did not complete within the time allotted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks




                After the listener is closed, the listener can safely be released.  
            



            This operation is allowed for listener in the   <b>WS_LISTENER_STATE_OPEN</b> or
                <b>WS_LISTENER_STATE_FAULTED</b> state.
            (For listener states, see the <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a> enumeration.) 

When a listener is closed, any pending attempts to accept a channel with the <a href="https://msdn.microsoft.com/e18e0005-89bd-435e-9a12-6602c3c638b7">WsAcceptChannel</a> method are aborted. However, <b>WsCloseListener</b> waits for any pending I/O to complete before proceeding with the closing process.
            
        



