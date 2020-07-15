---
UID: NN:netcon.IEnumNetSharingPrivateConnection
title: IEnumNetSharingPrivateConnection (netcon.h)
description: The IEnumNetSharingPrivateConnection interface provides methods for enumerating the currently configured privately-shared connections.
helpviewer_keywords: ["IEnumNetSharingPrivateConnection","IEnumNetSharingPrivateConnection interface [ICS/ICF]","IEnumNetSharingPrivateConnection interface [ICS/ICF]","described","_ics_ienumnetsharingprivateconnection","ics.ienumnetsharingprivateconnection","netcon/IEnumNetSharingPrivateConnection"]
old-location: ics\ienumnetsharingprivateconnection.htm
tech.root: ics
ms.assetid: 0e4cfa2e-8caa-4258-bd52-1f5a00403dfa
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingPrivateConnection, IEnumNetSharingPrivateConnection interface [ICS/ICF], IEnumNetSharingPrivateConnection interface [ICS/ICF],described, _ics_ienumnetsharingprivateconnection, ics.ienumnetsharingprivateconnection, netcon/IEnumNetSharingPrivateConnection
f1_keywords:
- netcon/IEnumNetSharingPrivateConnection
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
- IEnumNetSharingPrivateConnection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumNetSharingPrivateConnection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingPrivateConnection</b> interface provides methods for enumerating the currently configured privately-shared connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetSharingPrivateConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetSharingPrivateConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNetSharingPrivateConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-ienumnetsharingprivateconnection-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingprivateconnection-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of private connections from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingprivateconnection-reset">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingprivateconnection-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of private connections in this enumeration.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

