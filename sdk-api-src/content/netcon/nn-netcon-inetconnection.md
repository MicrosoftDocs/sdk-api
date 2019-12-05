---
UID: NN:netcon.INetConnection
title: INetConnection (netcon.h)
description: The INetConnection interface provides methods to manage network connections.
old-location: ics\inetconnection.htm
tech.root: ics
ms.assetid: 7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f
ms.date: 12/05/2018
ms.keywords: INetConnection, INetConnection interface [ICS/ICF], INetConnection interface [ICS/ICF],described, _ics_inetconnection, ics.inetconnection, netcon/INetConnection
ms.topic: interface
f1_keywords:
- netcon/INetConnection
dev_langs:
- c++
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Hnetcfg.dll
api_name:
- INetConnection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetConnection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetConnection</b> interface provides methods to manage network connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetconnection-connect">Connect</a>
</td>
<td align="left" width="63%">
Establish the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetconnection-delete">Delete</a>
</td>
<td align="left" width="63%">
Delete the network connection from the connections folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetconnection-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnect the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetconnection-duplicate">Duplicate</a>
</td>
<td align="left" width="63%">
Create a duplicate of the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetconnection-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieve the properties for the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetconnection-getuiobjectclassid">GetUiObjectClassId</a>
</td>
<td align="left" width="63%">
Retrieve the class identifier of the user interface for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetconnection-rename">Rename</a>
</td>
<td align="left" width="63%">
Rename the connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

