---
UID: NN:netfw.INetFwPolicy
title: INetFwPolicy (netfw.h)
description: The INetFwPolicy interface provides access to a firewall policy.
helpviewer_keywords: ["INetFwPolicy","INetFwPolicy interface [ICS/ICF]","INetFwPolicy interface [ICS/ICF]","described","ics.inetfwpolicy","netfw/INetFwPolicy"]
old-location: ics\inetfwpolicy.htm
tech.root: ics
ms.assetid: 8bfe55b6-c38d-47f8-9160-a304a85eb67f
ms.date: 12/05/2018
ms.keywords: INetFwPolicy, INetFwPolicy interface [ICS/ICF], INetFwPolicy interface [ICS/ICF],described, ics.inetfwpolicy, netfw/INetFwPolicy
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwPolicy
 - netfw/INetFwPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwPolicy
---

# INetFwPolicy interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwPolicy</b> interface  provides access to a firewall policy.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwPolicy</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwPolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwPolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy-get_currentprofile">get_CurrentProfile</a>
</td>
<td align="left" width="63%">
Retrieves the current profile in effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy-getprofilebytype">GetProfileByType</a>
</td>
<td align="left" width="63%">
Retrieves the profile currently in effect by type.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwPolicy</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwmgr-get_currentprofiletype">CurrentProfile</a>


</td>
<td align="left" width="63%">
Access to the type of firewall profile currently in effect.

</td>
</tr>
</table>

## -remarks

Instances of this interface are
retrieved through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-get_localpolicy">LocalPolicy</a> property of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwmgr">INetFwMgr</a> interface.

All configuration changes take
effect immediately.

The Windows Firewall/Internet Connection Sharing  service must be running to access this interface.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwmgr">INetFwMgr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

