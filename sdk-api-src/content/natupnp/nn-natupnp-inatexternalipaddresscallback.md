---
UID: NN:natupnp.INATExternalIPAddressCallback
title: INATExternalIPAddressCallback (natupnp.h)
description: The INATExternalIPAddressCallback interface is implemented by the NAT application with UPnP technology. It provides a method that the system calls if the external IP address of the NAT computer changes.
helpviewer_keywords: ["INATExternalIPAddressCallback","INATExternalIPAddressCallback interface [ICS/ICF]","INATExternalIPAddressCallback interface [ICS/ICF]","described","_ics_inatexternalipaddresscallback","ics.inatexternalipaddresscallback","natupnp/INATExternalIPAddressCallback"]
old-location: ics\inatexternalipaddresscallback.htm
tech.root: ics
ms.assetid: f180f597-680b-47ce-b437-3395069a8c77
ms.date: 12/05/2018
ms.keywords: INATExternalIPAddressCallback, INATExternalIPAddressCallback interface [ICS/ICF], INATExternalIPAddressCallback interface [ICS/ICF],described, _ics_inatexternalipaddresscallback, ics.inatexternalipaddresscallback, natupnp/INATExternalIPAddressCallback
req.header: natupnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - INATExternalIPAddressCallback
 - natupnp/INATExternalIPAddressCallback
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
 - INATExternalIPAddressCallback
---

# INATExternalIPAddressCallback interface


## -description

The 
<b>INATExternalIPAddressCallback</b> interface is implemented by the NAT application with UPnP technology. It provides a method that the system calls if the external IP address of the NAT computer changes.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INATExternalIPAddressCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INATExternalIPAddressCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INATExternalIPAddressCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-inatexternalipaddresscallback-newexternalipaddress">NewExternalIPAddress</a>
</td>
<td align="left" width="63%">
Notifies application when the NAT external address has changed.</p> (Inherited from <b>INATExternalIPAddressCallback</b>)</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inateventmanager">INATEventManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inatnumberofentriescallback">INATNumberOfEntriesCallback</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>

