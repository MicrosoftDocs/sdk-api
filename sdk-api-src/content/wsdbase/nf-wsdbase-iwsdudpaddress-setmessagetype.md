---
UID: NF:wsdbase.IWSDUdpAddress.SetMessageType
title: IWSDUdpAddress::SetMessageType (wsdbase.h)
description: Sets the message type for this UDP address configuration.
helpviewer_keywords: ["IWSDUdpAddress interface","SetMessageType method","IWSDUdpAddress.SetMessageType","IWSDUdpAddress::SetMessageType","SetMessageType","SetMessageType method","SetMessageType method","IWSDUdpAddress interface","ncd.iwsdudpaddress_setmessagetype","wsdbase/IWSDUdpAddress::SetMessageType"]
old-location: ncd\iwsdudpaddress_setmessagetype.htm
tech.root: ncd
ms.assetid: 1b041094-fb00-4b73-8753-cf89f9b10f97
ms.date: 12/05/2018
ms.keywords: IWSDUdpAddress interface,SetMessageType method, IWSDUdpAddress.SetMessageType, IWSDUdpAddress::SetMessageType, SetMessageType, SetMessageType method, SetMessageType method,IWSDUdpAddress interface, ncd.iwsdudpaddress_setmessagetype, wsdbase/IWSDUdpAddress::SetMessageType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDUdpAddress::SetMessageType
 - wsdbase/IWSDUdpAddress::SetMessageType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpAddress.SetMessageType
---

# IWSDUdpAddress::SetMessageType


## -description

Sets the message type for this UDP address configuration. There are two types of messages: one-way messages, which do not require responses, and two-way messages, which do require responses.

## -parameters

### -param messageType [in]

A <a href="/windows/desktop/api/wsdbase/ne-wsdbase-wsdudpmessagetype">WSDUdpMessageType</a> value that specifies the message type used for this address configuration.

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

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>