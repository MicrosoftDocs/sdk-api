---
UID: NN:wsdbase.IWSDHttpAddress
title: IWSDHttpAddress (wsdbase.h)
description: Provides access to the individual components of an HTTP address.
old-location: ncd\iwsdhttpaddress.htm
tech.root: WsdApi
ms.assetid: 79d3570a-56b2-40ad-b3c6-cddc3239da7e
ms.date: 12/05/2018
ms.keywords: IWSDHttpAddress, IWSDHttpAddress interface, IWSDHttpAddress interface,described, ncd.iwsdhttpaddress, wsdbase/IWSDHttpAddress
f1_keywords:
- wsdbase/IWSDHttpAddress
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
- IWSDHttpAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDHttpAddress interface


## -description


Provides access to the individual components of an HTTP address.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDHttpAddress</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdtransportaddress">IWSDTransportAddress</a>. <b>IWSDHttpAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDHttpAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpaddress-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Gets the URI path for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpaddress-getsecure">GetSecure</a>
</td>
<td align="left" width="63%">
Retrieves the status on whether TLS secure sessions are enabled for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpaddress-setpath">SetPath</a>
</td>
<td align="left" width="63%">
Sets the URI path for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpaddress-setsecure">SetSecure</a>
</td>
<td align="left" width="63%">
Enables or disables TLS secure sessions for this address.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdtransportaddress">IWSDTransportAddress</a>
 

 

