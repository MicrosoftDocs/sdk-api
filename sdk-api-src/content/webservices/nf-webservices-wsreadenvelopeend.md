---
UID: NF:webservices.WsReadEnvelopeEnd
title: WsReadEnvelopeEnd function
author: windows-sdk-content
description: Reads the closing elements of a message. The operation allows for reading of messages from sources other than Channels. If the source is a Channel use WsReadMessageEnd.
old-location: wsw\wsreadenvelopeend.htm
tech.root: wsw
ms.assetid: 1252fa10-d19a-4335-8dc5-f230141eef79
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsReadEnvelopeEnd, WsReadEnvelopeEnd function [Web Services for Windows], webservices/WsReadEnvelopeEnd, wsw.wsreadenvelopeend
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsReadEnvelopeEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsReadEnvelopeEnd function


## -description


Reads the closing elements of a message.
            
                The operation allows for reading of messages from sources other than Channels.  If the source is a Channel use <a href="https://msdn.microsoft.com/3112be44-f610-421f-a4ea-0f87fc383540">WsReadMessageEnd</a>.
            


## -parameters




### -param message [in]

A pointer to the <b>Message</b> object read.  The pointer must reference a valid <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a>.
                
                


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

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



The message state must be <b>WS_MESSAGE_STATE_READING</b>.  If called in the correct
                state the message state is set to  <b>WS_MESSAGE_STATE_DONE</b> regardless
                of function success or failure.
            



