---
UID: NF:webservices.WsAbandonMessage
title: WsAbandonMessage function
author: windows-sdk-content
description: Skips the remainder of a specified message on a specified channel.
old-location: wsw\wsabandonmessage.htm
old-project: wsw
ms.assetid: b8f5da50-d296-4550-8810-114d1f0e810b
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsAbandonMessage, WsAbandonMessage function [Web Services for Windows], webservices/WsAbandonMessage, wsw.wsabandonmessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
 - WsAbandonMessage
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAbandonMessage function


## -description




                Skips the remainder of a specified <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">message</a> on a specified channel.
            




## -parameters




### -param channel [in]

Pointer to a <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> structure representing the channel on which the message is being read or written.
                


### -param message [in]


                    Pointer to a <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure representing the message to abandon.  This should be
                    the same message that was passed to the <a href="https://msdn.microsoft.com/43cc43a5-7853-4170-911d-e514ac722da5">WsWriteMessageStart</a> 
                    or <a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> function.
                


### -param error [in, optional]


                    Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure that receives additional error information if the function fails.
                


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

                    The channel is not in the WS_CHANNEL_STATE_OPEN or  WS_CHANNEL_STATE_FAULTED state.
                (For channel states, see the <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE</a> enumeration.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

                    The specified message is not currently being read or written on the specified channel.
                

</td>
</tr>
</table>
 




## -remarks



<b>WsAbandonMessage</b> is used to skip reading or writing the remaining contents of a message, 
                allowing the next message for the channel to be read or written.  In this respect, it is an alternative to 
                the <a href="https://msdn.microsoft.com/3112be44-f610-421f-a4ea-0f87fc383540">WsReadMessageEnd</a> or <a href="https://msdn.microsoft.com/329193a7-932a-46d0-8e46-eef6bbdb8fa2">WsWriteMessageEnd</a> functions, as shown in the following
                state diagram:
            

<img alt="" src="./images/AbandonMessage.png"/>


                For read operations, an application typically calls <b>WsAbandonMessage</b> when it is unnecessary for the application to continue reading the 
                message data, for example, if the
                message does not meet the application's requirements.  This function can also be used 
                if the message contains malformed XML or if the <a href="https://msdn.microsoft.com/1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2">XML reader</a> has 
                generated an error while reading the message.  

If the channel is streamed 
                (see the WS_STREAMED_INPUT_TRANSFER_MODE value of the <a href="https://msdn.microsoft.com/6153bef6-f37f-4bc6-b1c5-5fbedd6bd234">WS_TRANSFER_MODE</a> enumeration),  the remainder of the 
                streamed message data is read and automatically discarded with the next call to 
                <a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> or <a href="https://msdn.microsoft.com/e4928371-a172-4cc8-968b-12ae2ee2e0c6">WsCloseChannel</a> for the 
                channel.  If the channel is not streamed, the unread buffered message data 
                is simply discarded.
            


                For write operations, an application typically calls <b>WsAbandonMessage</b> when the application cannot continue writing the message because it has encountered some error, such as one returned by the <a href="https://msdn.microsoft.com/69d50793-1d5b-4fc7-bf69-128f8e23a98d">XML writer</a>, or must stop generating the message for some other reason.  

If the 
                channel is streamed (see the WS_STREAMED_INPUT_TRANSFER_MODE value of the <a href="https://msdn.microsoft.com/6153bef6-f37f-4bc6-b1c5-5fbedd6bd234">WS_TRANSFER_MODE</a> enumeration), the message data will be truncated and may result in errors when read by the 
                remote party.  If the channel is not streamed,  the buffered data for the 
                message is simply  discarded (since it was never transmitted).
            


                This function allows the user of the channel to keep the channel open and 
                send or receive additional messages (such as sending a fault), even though 
                an error occurred.  In contrast, <a href="https://msdn.microsoft.com/67af85d7-db75-4e26-a7cc-8115ac3f2d59">WsAbortChannel</a> will causes 
                the channel to fault.  A typical usage is first to try to abandon the message and
                send a fault.  If that fails,  the channel can be aborted.
            


                This function does not perform any blocking I/O.
            


                This function is only valid when the channel is in the WS_CHANNEL_STATE_OPEN 
                 or WS_CHANNEL_STATE_FAULTED states.
            (For channel states, see the <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE</a> enumeration.)


                The message specified must be the current message being read or the current message being written
                for the specified channel.
            


                If called correctly, this function will not fail (for example, due to lack of system resources).
            



