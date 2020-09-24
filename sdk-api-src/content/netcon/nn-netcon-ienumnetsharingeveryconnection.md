---
UID: NN:netcon.IEnumNetSharingEveryConnection
title: IEnumNetSharingEveryConnection (netcon.h)
description: The IEnumNetSharingEveryConnection interface provides methods for enumerating all the connections in the Connections folder.
helpviewer_keywords: ["IEnumNetSharingEveryConnection","IEnumNetSharingEveryConnection interface [ICS/ICF]","IEnumNetSharingEveryConnection interface [ICS/ICF]","described","_ics_ienumnetsharingeveryconnection","ics.ienumnetsharingeveryconnection","netcon/IEnumNetSharingEveryConnection"]
old-location: ics\ienumnetsharingeveryconnection.htm
tech.root: ics
ms.assetid: d3be8047-e0d5-44b7-97d9-536bc4aa11c5
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingEveryConnection, IEnumNetSharingEveryConnection interface [ICS/ICF], IEnumNetSharingEveryConnection interface [ICS/ICF],described, _ics_ienumnetsharingeveryconnection, ics.ienumnetsharingeveryconnection, netcon/IEnumNetSharingEveryConnection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumNetSharingEveryConnection
 - netcon/IEnumNetSharingEveryConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - IEnumNetSharingEveryConnection
---

# IEnumNetSharingEveryConnection interface


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingEveryConnection</b> interface provides methods for enumerating all the connections in the Connections folder.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetSharingEveryConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetSharingEveryConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNetSharingEveryConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingeveryconnection-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingeveryconnection-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of private connections from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingeveryconnection-reset">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingeveryconnection-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of private connections in this enumeration.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>