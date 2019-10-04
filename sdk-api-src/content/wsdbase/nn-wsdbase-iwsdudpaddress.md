---
UID: NN:wsdbase.IWSDUdpAddress
title: IWSDUdpAddress (wsdbase.h)
author: windows-sdk-content
description: Provides access to the individual components of a UDP address.
old-location: ncd\iwsdudpaddress.htm
tech.root: WsdApi
ms.assetid: b666002f-2cd6-4e96-b055-34d801c1982e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDUdpAddress, IWSDUdpAddress interface, IWSDUdpAddress interface,described, ncd.iwsdudpaddress, wsdbase/IWSDUdpAddress
ms.topic: interface
f1_keywords: 
 - "wsdbase/IWSDUdpAddress"
dev_langs:
 - c++
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
 - IWSDUdpAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDUdpAddress interface


## -description


Provides access to the individual components of a UDP address.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDUdpAddress</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdtransportaddress">IWSDTransportAddress</a>. <b>IWSDUdpAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDUdpAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-getalias">GetAlias</a>
</td>
<td align="left" width="63%">
Gets the alias for the discovery address. This method is reserved for internal use and should not be called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-getexclusive">GetExclusive</a>
</td>
<td align="left" width="63%">
Determines whether the socket is in exclusive mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-getmessagetype">GetMessageType</a>
</td>
<td align="left" width="63%">
Gets the message type for this UDP address configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-getsockaddr">GetSockaddr</a>
</td>
<td align="left" width="63%">
Gets the socket address information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-getttl">GetTTL</a>
</td>
<td align="left" width="63%">
Gets the TTL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-setalias">SetAlias</a>
</td>
<td align="left" width="63%">
Sets the alias for the discovery address. This method is reserved for internal use and should not be called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-setexclusive">SetExclusive</a>
</td>
<td align="left" width="63%">
Controls whether the socket is in exclusive mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-setmessagetype">SetMessageType</a>
</td>
<td align="left" width="63%">
Sets the message type for this UDP address configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-setsockaddr">SetSockaddr</a>
</td>
<td align="left" width="63%">
Sets the socket address information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpaddress-setttl">SetTTL</a>
</td>
<td align="left" width="63%">
Sets the TTL.

</td>
</tr>
</table> 

