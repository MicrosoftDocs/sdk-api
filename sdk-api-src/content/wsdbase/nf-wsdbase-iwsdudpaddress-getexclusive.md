---
UID: NF:wsdbase.IWSDUdpAddress.GetExclusive
title: IWSDUdpAddress::GetExclusive (wsdbase.h)
description: Determines whether the socket is in exclusive mode.
helpviewer_keywords: ["GetExclusive","GetExclusive method","GetExclusive method","IWSDUdpAddress interface","IWSDUdpAddress interface","GetExclusive method","IWSDUdpAddress.GetExclusive","IWSDUdpAddress::GetExclusive","ncd.iwsdudpaddress_getexclusive","wsdbase/IWSDUdpAddress::GetExclusive"]
old-location: ncd\iwsdudpaddress_getexclusive.htm
tech.root: ncd
ms.assetid: 9ee62901-242a-47bc-a50d-4ced245392de
ms.date: 12/05/2018
ms.keywords: GetExclusive, GetExclusive method, GetExclusive method,IWSDUdpAddress interface, IWSDUdpAddress interface,GetExclusive method, IWSDUdpAddress.GetExclusive, IWSDUdpAddress::GetExclusive, ncd.iwsdudpaddress_getexclusive, wsdbase/IWSDUdpAddress::GetExclusive
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
 - IWSDUdpAddress::GetExclusive
 - wsdbase/IWSDUdpAddress::GetExclusive
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
 - IWSDUdpAddress.GetExclusive
---

# IWSDUdpAddress::GetExclusive


## -description

Determines whether the socket is in exclusive mode.



## -returns

Possible return values include, but are not limited to, the following:

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
The socket is in exclusive mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The socket is not in exclusive mode.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>
