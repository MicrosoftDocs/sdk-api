---
UID: NN:netcon.IEnumNetSharingPublicConnection
title: IEnumNetSharingPublicConnection (netcon.h)
author: windows-sdk-content
description: The IEnumNetSharingPublicConnection interface provides methods for enumerating the currently configured publicly-shared connections.
old-location: ics\ienumnetsharingpublicconnection.htm
tech.root: ics
ms.assetid: 69f2d4c0-7c25-4a50-988b-3ca6babb489a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingPublicConnection, IEnumNetSharingPublicConnection interface [ICS/ICF], IEnumNetSharingPublicConnection interface [ICS/ICF],described, _ics_ienumnetsharingpublicconnection, ics.ienumnetsharingpublicconnection, netcon/IEnumNetSharingPublicConnection
ms.topic: interface
f1_keywords: 
 - "netcon/IEnumNetSharingPublicConnection"
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
 - IEnumNetSharingPublicConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumNetSharingPublicConnection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingPublicConnection</b> interface provides methods for enumerating the currently configured publicly-shared connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetSharingPublicConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetSharingPublicConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNetSharingPublicConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingpublicconnection-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingpublicconnection-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of public connections from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingpublicconnection-reset">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingpublicconnection-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of public connections in this enumeration.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

