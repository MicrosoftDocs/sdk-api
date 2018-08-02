---
UID: NN:wtsprotocol.IWTSProtocolLicenseConnection
title: IWTSProtocolLicenseConnection
author: windows-sdk-content
description: IWTSProtocolLicenseConnection is no longer available. Instead, use IWRdsProtocolLicenseConnection.
old-location: termserv\iwtsprotocollicenseconnection.htm
old-project: TermServ
ms.assetid: 3f6925b6-c712-40c6-8b48-7df8ef4a9872
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWTSProtocolLicenseConnection, IWTSProtocolLicenseConnection interface [Remote Desktop Services], IWTSProtocolLicenseConnection interface [Remote Desktop Services],described, termserv.iwtsprotocollicenseconnection, wtsprotocol/IWTSProtocolLicenseConnection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWTSProtocolLicenseConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolLicenseConnection interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a>.]

Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence. This interface is implemented by the protocol, and its methods are called by the Remote Desktop Services service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolLicenseConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSProtocolLicenseConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolLicenseConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a615e25-51d0-49eb-ae0f-185fd3a0ea23">ProtocolComplete</a>
</td>
<td align="left" width="63%">
Notifies the protocol whether the licensing process completed successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4740d7a4-aa82-4c9d-b93c-20a974f170ae">RequestClientLicense</a>
</td>
<td align="left" width="63%">
Requests a license from the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff6123f6-4d78-41d1-8093-916f01de09ef">RequestLicensingCapabilities</a>
</td>
<td align="left" width="63%">
Requests license capabilities from the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cafd23ed-2085-4d58-a9b1-1918995fa09c">SendClientLicense</a>
</td>
<td align="left" width="63%">
Sends a license to the client.

</td>
</tr>
</table> 

