---
UID: NF:wsdbase.IWSDUdpAddress.GetSockaddr
title: IWSDUdpAddress::GetSockaddr (wsdbase.h)
description: Gets the socket address information.
helpviewer_keywords: ["GetSockaddr","GetSockaddr method","GetSockaddr method","IWSDUdpAddress interface","IWSDUdpAddress interface","GetSockaddr method","IWSDUdpAddress.GetSockaddr","IWSDUdpAddress::GetSockaddr","ncd.iwsdudpaddress_getsockaddr","wsdbase/IWSDUdpAddress::GetSockaddr"]
old-location: ncd\iwsdudpaddress_getsockaddr.htm
tech.root: ncd
ms.assetid: 4a29722f-a3b7-4285-9ade-06de125f8b91
ms.date: 12/05/2018
ms.keywords: GetSockaddr, GetSockaddr method, GetSockaddr method,IWSDUdpAddress interface, IWSDUdpAddress interface,GetSockaddr method, IWSDUdpAddress.GetSockaddr, IWSDUdpAddress::GetSockaddr, ncd.iwsdudpaddress_getsockaddr, wsdbase/IWSDUdpAddress::GetSockaddr
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
 - IWSDUdpAddress::GetSockaddr
 - wsdbase/IWSDUdpAddress::GetSockaddr
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
 - IWSDUdpAddress.GetSockaddr
---

# IWSDUdpAddress::GetSockaddr


## -description

Gets the socket address information.

## -parameters

### -param pSockAddr [out]

Pointer to a <a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a> structure that contains the address information.

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
<i>pSockAddr</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a>