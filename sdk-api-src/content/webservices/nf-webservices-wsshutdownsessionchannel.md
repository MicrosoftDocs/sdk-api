---
UID: NF:webservices.WsShutdownSessionChannel
title: WsShutdownSessionChannel function
author: windows-sdk-content
description: Used to signal the end of messages for a session channel.
old-location: wsw\wsshutdownsessionchannel.htm
tech.root: wsw
ms.assetid: db12b0b7-698e-4c74-b547-6c95d0c5fdb7
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WsShutdownSessionChannel, WsShutdownSessionChannel function [Web Services for Windows], webservices/WsShutdownSessionChannel, wsw.wsshutdownsessionchannel
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
 - WsShutdownSessionChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsShutdownSessionChannel function


## -description


Used to signal the end of messages for a session channel.
            


## -parameters




### -param channel [in]

The session channel to shut down.
                


### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.
                


### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
This is returned if the channel is not in the <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_OPEN</a>state.
                

</td>
</tr>
</table>
 




## -remarks



This function will indicate to the remote party that all
                messages have been sent for the channel.
            

The remote party can detect that no more messages are available on the channel by 
                looking for the <b>WS_S_END</b> return value when receiving a message. (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) However, 
                messages can also become unavailable if the non-application messages were filtered by 
                the channel as described in <a href="https://msdn.microsoft.com/d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19">Channel Layer Overview</a>. Session shutdown can 
                be distinguished from message filtering by keeping track of whether prior messages were 
                received. If prior messages were received then the session was shut down.


This function only applies to channels created with a
                <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE</a> with a session that support
                sending of messages:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_OUTPUT_SESSION</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_DUPLEX_SESSION</a>
</li>
</ul>
The channel must be in <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_OPEN</a> state.
            

If this function is successful, the value of the
                <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_IS_SESSION_SHUT_DOWN</a> property
                will be <b>TRUE</b>.
            

Once a session channel has been shut down, attempting
                to send a message on the channel or attempting to shut down
                the channel will return <b>WS_E_INVALID_OPERATION</b>.
            

Calling this function is optional.  When a session channel is closed using 
                <a href="https://msdn.microsoft.com/e4928371-a172-4cc8-968b-12ae2ee2e0c6">WsCloseChannel</a> when in <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_OPEN</a>,
                then the channel is automatically shut down as part of the close process.
            



