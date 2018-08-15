---
UID: NN:wsdbase.IWSDHttpMessageParameters
title: IWSDHttpMessageParameters
author: windows-sdk-content
description: Provides access to the HTTP headers used when transmitting messages via SOAP-over-HTTP.
old-location: ncd\iwsdhttpmessageparameters.htm
old-project: wsdapi
ms.assetid: fae10e9e-0c2b-4817-bd28-a4a85ca180cc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWSDHttpMessageParameters, IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,described, ncd.iwsdhttpmessageparameters, wsdbase/IWSDHttpMessageParameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.redist: 
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
 - IWSDHttpMessageParameters
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDHttpMessageParameters interface


## -description


Provides access to the HTTP headers used when transmitting messages via SOAP-over-HTTP.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDHttpMessageParameters</b> interface inherits from <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>. <b>IWSDHttpMessageParameters</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e5cd5c07-3326-4508-89ac-939466381b12">Clear</a>
</td>
<td align="left" width="63%">
Clears the HTTP headers used for SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af93f97f-a3de-4b5c-92c5-2d4ab91e7985">GetContext</a>
</td>
<td align="left" width="63%">
Retrieves the private transmission context for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbe7000f-271a-4939-814d-3696d29f7a41">GetID</a>
</td>
<td align="left" width="63%">
Retrieves the transport ID for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99b30444-1059-45c3-ac72-a0f98d722365">GetInboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the current HTTP headers used for incoming SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c366773a-1869-4181-a457-560a1a9c84cd">GetOutboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the current HTTP headers used for outbound SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e1bbfbe-b7a7-4235-bb2d-8ee0ef301871">SetContext</a>
</td>
<td align="left" width="63%">
Sets the private transmission context for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a05239-f1d5-4bd8-8aec-1e641397caa0">SetID</a>
</td>
<td align="left" width="63%">
Sets the transport ID for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd680016-1e6f-4d15-b1ca-cd2b6b210a71">SetInboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Sets the HTTP headers used for incoming SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f54f86dc-4b25-4faa-8a37-b241e9ba8c6c">SetOutboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Sets the HTTP headers used for outbound SOAP-over-HTTP transmissions.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>
 

 

