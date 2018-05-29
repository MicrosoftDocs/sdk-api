---
UID: NN:wsdbase.IWSDUdpAddress
title: IWSDUdpAddress
author: windows-sdk-content
description: Provides access to the individual components of a UDP address.
old-location: ncd\iwsdudpaddress.htm
old-project: WsdApi
ms.assetid: b666002f-2cd6-4e96-b055-34d801c1982e
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSDUdpAddress, IWSDUdpAddress interface, IWSDUdpAddress interface,described, ncd.iwsdudpaddress, wsdbase/IWSDUdpAddress
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDUdpAddress
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDUdpAddress interface


## -description


Provides access to the individual components of a UDP address.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDUdpAddress</b> interface inherits from <a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a>. <b>IWSDUdpAddress</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c11a7e39-6df1-411b-9992-6ce869b0db69">GetAlias</a>
</td>
<td align="left" width="63%">
Gets the alias for the discovery address. This method is reserved for internal use and should not be called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ee62901-242a-47bc-a50d-4ced245392de">GetExclusive</a>
</td>
<td align="left" width="63%">
Determines whether the socket is in exclusive mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/258d7067-9b2b-4375-8b1a-c1d45cf55788">GetMessageType</a>
</td>
<td align="left" width="63%">
Gets the message type for this UDP address configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a29722f-a3b7-4285-9ade-06de125f8b91">GetSockaddr</a>
</td>
<td align="left" width="63%">
Gets the socket address information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bc2a973-a776-45c6-b6bf-cf268badab30">GetTTL</a>
</td>
<td align="left" width="63%">
Gets the TTL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2156f271-cad4-4160-8d1f-bc44dc7b0e9f">SetAlias</a>
</td>
<td align="left" width="63%">
Sets the alias for the discovery address. This method is reserved for internal use and should not be called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08c5ee4a-55a4-4d8b-951e-d7faed45f44f">SetExclusive</a>
</td>
<td align="left" width="63%">
Controls whether the socket is in exclusive mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b041094-fb00-4b73-8753-cf89f9b10f97">SetMessageType</a>
</td>
<td align="left" width="63%">
Sets the message type for this UDP address configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8c6cc53-bba6-44ef-8c1e-f357e11793b4">SetSockaddr</a>
</td>
<td align="left" width="63%">
Sets the socket address information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fcd8dd1-a00c-4085-a608-cb680285d869">SetTTL</a>
</td>
<td align="left" width="63%">
Sets the TTL.

</td>
</tr>
</table> 

