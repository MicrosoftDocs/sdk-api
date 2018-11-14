---
UID: NF:webservices.WsResetMessage
title: WsResetMessage function
author: windows-sdk-content
description: Sets the Message state back to WS_MESSAGE_STATE_EMPTY. In this state the Message object can be reused.
old-location: wsw\wsresetmessage.htm
tech.root: wsw
ms.assetid: 90a62cc8-a7e0-4451-8490-f6384bf3e7b6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsResetMessage, WsResetMessage function [Web Services for Windows], webservices/WsResetMessage, wsw.wsresetmessage
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
 - WsResetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WsResetMessage
: 
---

# WsResetMessage function


## -description


Sets the Message state back to <b>WS_MESSAGE_STATE_EMPTY</b>.  In this state the Message object can be reused.
            


## -parameters




### -param message [in]

A pointer to the Message  object to reset.  
                    


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
</table>
 




## -remarks



When a message is reset, its underlying heap is reset.
            

Reusing a message object to receive or send multiple messages is is generally
                more efficient than creating and free'ing the message object for each message.
            



