---
UID: NN:wsdbase.IWSDHttpMessageParameters
title: IWSDHttpMessageParameters (wsdbase.h)

description: Provides access to the HTTP headers used when transmitting messages via SOAP-over-HTTP.
old-location: ncd\iwsdhttpmessageparameters.htm
tech.root: WsdApi
ms.assetid: fae10e9e-0c2b-4817-bd28-a4a85ca180cc

ms.date: 12/05/2018
ms.keywords: IWSDHttpMessageParameters, IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,described, ncd.iwsdhttpmessageparameters, wsdbase/IWSDHttpMessageParameters
ms.topic: interface
f1_keywords: 
 - "wsdbase/IWSDHttpMessageParameters"
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
 - IWSDHttpMessageParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDHttpMessageParameters interface


## -description


Provides access to the HTTP headers used when transmitting messages via SOAP-over-HTTP.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDHttpMessageParameters</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>. <b>IWSDHttpMessageParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDHttpMessageParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the HTTP headers used for SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Retrieves the private transmission context for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-getid">GetID</a>
</td>
<td align="left" width="63%">
Retrieves the transport ID for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-getinboundhttpheaders">GetInboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the current HTTP headers used for incoming SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-getoutboundhttpheaders">GetOutboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the current HTTP headers used for outbound SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Sets the private transmission context for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-setid">SetID</a>
</td>
<td align="left" width="63%">
Sets the transport ID for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-setinboundhttpheaders">SetInboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Sets the HTTP headers used for incoming SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpmessageparameters-setoutboundhttpheaders">SetOutboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Sets the HTTP headers used for outbound SOAP-over-HTTP transmissions.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>
 

 

