---
UID: NF:webservices.WsRequestSecurityToken
title: WsRequestSecurityToken function
author: windows-sdk-content
description: Get a security token from a security token service (STS) that acts as the token issuer in a federation scenario.
old-location: wsw\wsrequestsecuritytoken.htm
tech.root: wsw
ms.assetid: ee754a7d-73a9-49ae-afc7-b443fbbe0cce
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsRequestSecurityToken, WsRequestSecurityToken function [Web Services for Windows], webservices/WsRequestSecurityToken, wsw.wsrequestsecuritytoken
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
 - WsRequestSecurityToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WsRequestSecurityToken
: 
---

# WsRequestSecurityToken function


## -description


Get a security token from a security token service (STS) that acts as
the token issuer in a federation scenario.
This function is used on the client side, and performs the WS-Trust
based negotiation steps with the STS until the security token is
obtained or the negotiation process fails.
            


## -parameters




### -param channel [in]

The channel on which the negotiation to obtain the security token
should take place.
                

The supplied channel should have been <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">created</a> with the appropriate <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">WS_SECURITY_DESCRIPTION</a> to meet the security requirements of
the issuer, and then <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">opened</a> to the <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> of the issuer.  The caller is also
responsible for <a href="https://msdn.microsoft.com/e4928371-a172-4cc8-968b-12ae2ee2e0c6">closing</a> and <a href="https://msdn.microsoft.com/74e36d19-c6db-4bba-90e3-88a48b6a1fb5">freeing</a> the channel after the completion of
this function.
                

Thus, the channel must be in state <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_OPEN</a>when this function is called.  After a successful completion of this
function, the channel will be in state <b>WS_CHANNEL_STATE_OPEN</b>.  After a failed completion, it will
either be in state <b>WS_CHANNEL_STATE_OPEN</b> or state <b>WS_CHANNEL_STATE_FAULTED</b>.
                


### -param properties

An optional group of settings to be used in the negotiation process
with the issuer.
                


### -param propertyCount [in]

The number of items in the properties array.
                


### -param token

The XML security token obtained.  This is set upon successful
completion of the function call, and is unmodified if any failure
occurs during the execution of the function.
                

The returned security token may be used with <a href="https://msdn.microsoft.com/5ca1e67a-11f5-44bb-afe8-c934837d711b">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a> if it is to be
presented to a service.  The token must be freed using <a href="https://msdn.microsoft.com/7f9500a8-b54f-4967-8f8d-9f8770d3dd60">WsFreeSecurityToken</a> when it is no longer needed.
                


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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

</td>
</tr>
</table>
 




## -remarks



Windows 7 and Windows Server 2008 R2: WWSAPI only supports <a href="http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf">Ws-Trust</a> and <a href="http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf">Ws-SecureConversation</a> as defined by <a href="http://msdn.microsoft.com/en-us/library/dd357239(PROT.10).aspx">Lightweight Web Services Security Profile (LWSSP)</a>. For details regarding Microsoft's implementation please see the <a href="http://msdn.microsoft.com/en-us/library/dd341306(v=PROT.10).aspx">MESSAGE Syntax</a> section of LWSSP.



