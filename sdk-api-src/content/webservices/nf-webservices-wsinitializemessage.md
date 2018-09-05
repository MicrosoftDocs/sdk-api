---
UID: NF:webservices.WsInitializeMessage
title: WsInitializeMessage function
author: windows-sdk-content
description: This function initializes the headers for the message in preparation for processing.
old-location: wsw\wsinitializemessage.htm
old-project: wsw
ms.assetid: 26eafc5f-6636-4f96-a037-7935cdac5900
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WsInitializeMessage, WsInitializeMessage function [Web Services for Windows], webservices/WsInitializeMessage, wsw.wsinitializemessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.redist: 
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsInitializeMessage
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsInitializeMessage function


## -description


This function initializes the headers for the message in preparation for
                processing.
            After a message has been initialized an application can
                add additional headers.
            On success the message is in <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_INITIALIZED</a> state.
                If the function fails, then no state transitions occurs.
            


## -parameters




### -param message [in]

A pointer to the Message object to initialize.  The Message must be a valid <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> object instance returned
                    by <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> or <a href="https://msdn.microsoft.com/0a4f076b-6725-45a9-8817-5dec3b647c4f">WsCreateMessageForChannel</a> and may not be NULL.
                


### -param initialization [in]

Defines the Message initialization. 
                

<div class="alert"><b>Note</b>  If the  <i>initialization</i> value is set to <b>WS_REPLY_MESSAGE</b> or
                <b>WS_FAULT_MESSAGE</b> the message is automatically addressed.
            </div>
<div> </div>

### -param sourceMessage [in, optional]

A pointer to a message object that is used to initialize the <i>message</i> parameter.
                    This value should be NULL unless the initialization parameter
                    has the value of <b>WS_DUPLICATE_MESSAGE</b>,
                    <b>WS_REPLY_MESSAGE</b>, or <b>WS_FAULT_MESSAGE</b>.
                


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



The initial sender of a message should add an action header
                to the message using <a href="https://msdn.microsoft.com/34671c47-d21e-47c4-9fb0-10b036fb4f70">WsSetHeader</a>.
            

This API must be called before <a href="https://msdn.microsoft.com/213fe780-82f2-4140-92f2-2665317a5cb6">WsWriteEnvelopeStart</a> or
                <a href="https://msdn.microsoft.com/43cc43a5-7853-4170-911d-e514ac722da5">WsWriteMessageStart</a> is called for the message.
            



