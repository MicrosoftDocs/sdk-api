---
UID: NN:wsdbase.IWSDMessageParameters
title: IWSDMessageParameters
author: windows-sdk-content
description: Use this interface to communicate message specific information up and down the protocol stack.
old-location: ncd\iwsdmessageparameters.htm
old-project: WsdApi
ms.assetid: fb659a5e-1f55-47a6-b22d-660975d8c0fd
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSDMessageParameters, IWSDMessageParameters interface, IWSDMessageParameters interface,described, ncd.iwsdmessageparameters, wsdbase/IWSDMessageParameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDMessageParameters
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDMessageParameters interface


## -description


Use this interface to communicate message specific information up and down the protocol stack. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDMessageParameters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDMessageParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDMessageParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97eab68f-9a77-46ae-a50e-be6267e25040">GetLocalAddress</a>
</td>
<td align="left" width="63%">
Retrieves the generic address object representing the local address that received the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24f4be83-adf4-4742-8a1e-4304870a16dc">GetLowerParameters</a>
</td>
<td align="left" width="63%">
Retrieves message parameters from the layer below this layer in the protocol stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/483306d4-9672-4f30-a318-df5c7afbf583">GetRemoteAddress</a>
</td>
<td align="left" width="63%">
Retrieves the generic address object representing the remote address from which the message was sent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8266f091-9c88-44eb-a32b-1ff3da5fa10e">SetLocalAddress</a>
</td>
<td align="left" width="63%">
Sets a generic address object representing the source address that should send the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e762942-37b2-43ca-96e3-98594b929d98">SetRemoteAddress</a>
</td>
<td align="left" width="63%">
Sets the generic address object representing the remote address to where the message is sent.

</td>
</tr>
</table> 


## -remarks



In a request-response message pattern, the parameters also provide a way for the transport to determine where the response message for a given request should be sent. To enable this, the message parameters for a request must always be passed down the stack with the corresponding response.

Since message parameters can be packaged with a request or a response, and can be sent or received, the meaning of the local and remote address depends on the direction the message parameters.



