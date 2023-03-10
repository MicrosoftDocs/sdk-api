---
UID: NF:wsdbase.IWSDUdpAddress.GetMessageType
title: IWSDUdpAddress::GetMessageType (wsdbase.h)
description: Gets the message type for this UDP address configuration.
helpviewer_keywords: ["GetMessageType","GetMessageType method","GetMessageType method","IWSDUdpAddress interface","IWSDUdpAddress interface","GetMessageType method","IWSDUdpAddress.GetMessageType","IWSDUdpAddress::GetMessageType","ncd.iwsdudpaddress_getmessagetype","wsdbase/IWSDUdpAddress::GetMessageType"]
old-location: ncd\iwsdudpaddress_getmessagetype.htm
tech.root: ncd
ms.assetid: 258d7067-9b2b-4375-8b1a-c1d45cf55788
ms.date: 12/05/2018
ms.keywords: GetMessageType, GetMessageType method, GetMessageType method,IWSDUdpAddress interface, IWSDUdpAddress interface,GetMessageType method, IWSDUdpAddress.GetMessageType, IWSDUdpAddress::GetMessageType, ncd.iwsdudpaddress_getmessagetype, wsdbase/IWSDUdpAddress::GetMessageType
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
 - IWSDUdpAddress::GetMessageType
 - wsdbase/IWSDUdpAddress::GetMessageType
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
 - IWSDUdpAddress.GetMessageType
---

# IWSDUdpAddress::GetMessageType


## -description

Gets the message type for this UDP address configuration. There are two types of messages; one-way messages, which do not require responses, and two-way messages, which do require responses.

## -parameters

### -param pMessageType [out]

Pointer to a <a href="/windows/desktop/api/wsdbase/ne-wsdbase-wsdudpmessagetype">WSDUdpMessageType</a> value that specifies the message type used for this address configuration.

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

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>