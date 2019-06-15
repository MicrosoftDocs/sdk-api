---
UID: NN:wtsprotocol.IWRdsProtocolLicenseConnection
title: IWRdsProtocolLicenseConnection (wtsprotocol.h)
author: windows-sdk-content
description: Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.
old-location: termserv\iwrdsprotocollicenseconnection.htm
tech.root: TermServ
ms.assetid: 498c31c5-1cb6-41d7-91fb-7409ea03dda0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLicenseConnection, IWRdsProtocolLicenseConnection interface [Remote Desktop Services], IWRdsProtocolLicenseConnection interface [Remote Desktop Services],described, termserv.iwrdsprotocollicenseconnection, wtsprotocol/IWRdsProtocolLicenseConnection
ms.topic: interface
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolLicenseConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolLicenseConnection interface


## -description


Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence. This interface is implemented by the protocol, and its methods are called by the Remote Desktop Services service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolLicenseConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolLicenseConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolLicenseConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-protocolcomplete">ProtocolComplete</a>
</td>
<td align="left" width="63%">
Notifies the protocol whether the licensing process completed successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-requestclientlicense">RequestClientLicense</a>
</td>
<td align="left" width="63%">
Requests a license from the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-requestlicensingcapabilities">RequestLicensingCapabilities</a>
</td>
<td align="left" width="63%">
Requests license capabilities from the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollicenseconnection-sendclientlicense">SendClientLicense</a>
</td>
<td align="left" width="63%">
Sends a license to the client.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



