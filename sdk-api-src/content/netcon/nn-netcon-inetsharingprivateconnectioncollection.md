---
UID: NN:netcon.INetSharingPrivateConnectionCollection
title: INetSharingPrivateConnectionCollection (netcon.h)
description: The INetSharingPrivateConnectionCollection interface makes it possible for scripting languages such as VBScript and JScript to enumerate private connections.
helpviewer_keywords: ["INetSharingPrivateConnectionCollection","INetSharingPrivateConnectionCollection interface [ICS/ICF]","INetSharingPrivateConnectionCollection interface [ICS/ICF]","described","_ics_inetsharingprivateconnectioncollection","ics.inetsharingprivateconnectioncollection","netcon/INetSharingPrivateConnectionCollection"]
old-location: ics\inetsharingprivateconnectioncollection.htm
tech.root: ics
ms.assetid: 6e850e7b-841a-4f14-bab2-4a5a67dcb360
ms.date: 12/05/2018
ms.keywords: INetSharingPrivateConnectionCollection, INetSharingPrivateConnectionCollection interface [ICS/ICF], INetSharingPrivateConnectionCollection interface [ICS/ICF],described, _ics_inetsharingprivateconnectioncollection, ics.inetsharingprivateconnectioncollection, netcon/INetSharingPrivateConnectionCollection
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
 - INetSharingPrivateConnectionCollection
 - netcon/INetSharingPrivateConnectionCollection
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
 - INetSharingPrivateConnectionCollection
---

# INetSharingPrivateConnectionCollection interface


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingPrivateConnectionCollection</b> interface makes it possible for scripting languages such as VBScript and JScript to enumerate private connections.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPrivateConnectionCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingPrivateConnectionCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPrivateConnectionCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netcon/nf-netcon-inetsharingprivateconnectioncollection-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the private connections collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingprivateconnectioncollection-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the private connections collection.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>