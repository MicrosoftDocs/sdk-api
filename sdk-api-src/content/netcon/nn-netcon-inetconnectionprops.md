---
UID: NN:netcon.INetConnectionProps
title: INetConnectionProps (netcon.h)

description: Use the INetConnectionProps interface to retrieve the properties for a connection.
old-location: ics\inetconnectionprops.htm
tech.root: ics
ms.assetid: 8152f75c-1c93-4c30-8a13-c47fd5dde4af

ms.date: 12/05/2018
ms.keywords: INetConnectionProps, INetConnectionProps interface [ICS/ICF], INetConnectionProps interface [ICS/ICF],described, _ics_inetconnectionprops, ics.inetconnectionprops, netcon/INetConnectionProps
ms.topic: interface
f1_keywords: 
 - "netcon/INetConnectionProps"
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
 - INetConnectionProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetConnectionProps interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

Use the 
<b>INetConnectionProps</b> interface to retrieve the properties for a connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetConnectionProps</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetConnectionProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetConnectionProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetconnectionprops-get_devicename">get_DeviceName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device associated with the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetconnectionprops-get_guid">get_Guid</a>
</td>
<td align="left" width="63%">
Retrieves the globally-unique identifier (GUID) for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetconnectionprops-get_mediatype">get_MediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetconnectionprops-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetconnectionprops-get_status">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the status of the connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_netconnectionprops">INetSharingManager::get_NetConnectionProps</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

