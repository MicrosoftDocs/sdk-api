---
UID: NN:netcon.INetSharingPublicConnectionCollection
title: INetSharingPublicConnectionCollection (netcon.h)
description: The INetSharingPublicConnectionCollection interface makes it possible for scripting languages such as VBScript and JScript to enumerate public connections.
helpviewer_keywords: ["INetSharingPublicConnectionCollection","INetSharingPublicConnectionCollection interface [ICS/ICF]","INetSharingPublicConnectionCollection interface [ICS/ICF]","described","_ics_inetsharingpublicconnectioncollection","ics.inetsharingpublicconnectioncollection","netcon/INetSharingPublicConnectionCollection"]
old-location: ics\inetsharingpublicconnectioncollection.htm
tech.root: ics
ms.assetid: 92027ba2-b803-4c9f-ae77-a89074fef718
ms.date: 12/05/2018
ms.keywords: INetSharingPublicConnectionCollection, INetSharingPublicConnectionCollection interface [ICS/ICF], INetSharingPublicConnectionCollection interface [ICS/ICF],described, _ics_inetsharingpublicconnectioncollection, ics.inetsharingpublicconnectioncollection, netcon/INetSharingPublicConnectionCollection
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
 - INetSharingPublicConnectionCollection
 - netcon/INetSharingPublicConnectionCollection
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
 - INetSharingPublicConnectionCollection
---

# INetSharingPublicConnectionCollection interface


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingPublicConnectionCollection</b> interface makes it possible for scripting languages such as VBScript and JScript to enumerate public connections.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPublicConnectionCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingPublicConnectionCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPublicConnectionCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingpublicconnectioncollection-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the public connections collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingpublicconnectioncollection-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the public connections collection.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>