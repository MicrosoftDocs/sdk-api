---
UID: NF:wsdbase.IWSDUdpAddress.GetMessageType
title: IWSDUdpAddress::GetMessageType
author: windows-sdk-content
description: Gets the message type for this UDP address configuration.
old-location: ncd\iwsdudpaddress_getmessagetype.htm
old-project: wsdapi
ms.assetid: 258d7067-9b2b-4375-8b1a-c1d45cf55788
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMessageType, GetMessageType method, GetMessageType method,IWSDUdpAddress interface, IWSDUdpAddress interface,GetMessageType method, IWSDUdpAddress.GetMessageType, IWSDUdpAddress::GetMessageType, ncd.iwsdudpaddress_getmessagetype, wsdbase/IWSDUdpAddress::GetMessageType
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpAddress.GetMessageType
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDUdpAddress::GetMessageType


## -description


Gets the message type for this UDP address configuration. There are two types of messages; one-way messages, which do not require responses, and two-way messages, which do require responses.


## -parameters




### -param pMessageType [out]

Pointer to a <a href="https://msdn.microsoft.com/0af4fd37-b1a9-4916-986c-e071c060d020">WSDUdpMessageType</a> value that specifies the message type used for this address configuration.


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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pMessageType</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>
 

 

