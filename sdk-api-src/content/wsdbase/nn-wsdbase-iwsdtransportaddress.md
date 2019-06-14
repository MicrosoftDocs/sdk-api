---
UID: NN:wsdbase.IWSDTransportAddress
title: IWSDTransportAddress (wsdbase.h)
author: windows-sdk-content
description: Represents an IP-based transport address.
old-location: ncd\iwsdtransportaddress.htm
tech.root: WsdApi
ms.assetid: 84dfee11-8092-4018-8840-e766a94c60a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDTransportAddress, IWSDTransportAddress interface, IWSDTransportAddress interface,described, ncd.iwsdtransportaddress, wsdbase/IWSDTransportAddress
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDTransportAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDTransportAddress interface


## -description


Represents an IP-based transport address.

You should not create an instance of the <b>IWSDTransportAddress</b> interface. Instead, create an instance of either the <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdudpaddress">IWSDUdpAddress</a> interface if an address object is required.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDTransportAddress</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a>. <b>IWSDTransportAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDTransportAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdtransportaddress-getport">GetPort</a>
</td>
<td align="left" width="63%">
Gets the IP port number associated with this transport address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdtransportaddress-gettransportaddress">GetTransportAddress</a>
</td>
<td align="left" width="63%">
Gets a pointer to a string representation of the address object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdtransportaddress-gettransportaddressex">GetTransportAddressEx</a>
</td>
<td align="left" width="63%">
Gets a pointer to a string representation of the address object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdtransportaddress-setport">SetPort</a>
</td>
<td align="left" width="63%">
Sets the IP port number for this transport address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdtransportaddress-settransportaddress">SetTransportAddress</a>
</td>
<td align="left" width="63%">
Sets the string representation of the transport address. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a>
 

 

