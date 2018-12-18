---
UID: NF:wsdbase.IWSDUdpAddress.SetMessageType
title: IWSDUdpAddress::SetMessageType
author: windows-sdk-content
description: Sets the message type for this UDP address configuration.
old-location: ncd\iwsdudpaddress_setmessagetype.htm
tech.root: wsdapi
ms.assetid: 1b041094-fb00-4b73-8753-cf89f9b10f97
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDUdpAddress interface,SetMessageType method, IWSDUdpAddress.SetMessageType, IWSDUdpAddress::SetMessageType, SetMessageType, SetMessageType method, SetMessageType method,IWSDUdpAddress interface, ncd.iwsdudpaddress_setmessagetype, wsdbase/IWSDUdpAddress::SetMessageType
ms.topic: method
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpAddress.SetMessageType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDUdpAddress::SetMessageType


## -description


Sets the message type for this UDP address configuration. There are two types of messages: one-way messages, which do not require responses, and two-way messages, which do require responses.


## -parameters




### -param messageType [in]

A <a href="https://msdn.microsoft.com/0af4fd37-b1a9-4916-986c-e071c060d020">WSDUdpMessageType</a> value that specifies the message type used for this address configuration.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>
 

 

