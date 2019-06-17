---
UID: NN:netfw.INetFwMgr
title: INetFwMgr (netfw.h)
author: windows-sdk-content
description: The INetFwMgr interface provides access to the firewall settings for a computer.
old-location: ics\inetfwmgr.htm
tech.root: ics
ms.assetid: 7534ea10-7553-4ec2-af68-0b0393ffc003
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwMgr, INetFwMgr interface [ICS/ICF], INetFwMgr interface [ICS/ICF],described, ics.inetfwmgr, netfw/INetFwMgr
ms.topic: interface
f1_keywords: ["netfw/INetFwMgr"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwMgr interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservices">INetFwMgr</a> interface  provides access to the firewall settings for a computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwMgr</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwmgr-get_currentprofiletype">get_CurrentProfileType</a>
</td>
<td align="left" width="63%">
Retrieves the type of firewall profile currently in effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-get_localpolicy">get_LocalPolicy</a>
</td>
<td align="left" width="63%">
Retrieves the local firewall policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-isicmptypeallowed">IsIcmpTypeAllowed</a>
</td>
<td align="left" width="63%">
Determines whether the specified ICMP type is allowed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-isportallowed">IsPortAllowed</a>
</td>
<td align="left" width="63%">
Determines whether an application can listen for inbound traffic on the specified port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-restoredefaults">RestoreDefaults</a>
</td>
<td align="left" width="63%">
Restores the local configuration to its default state.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwMgr</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwmgr-get_currentprofiletype">CurrentProfileType</a>


</td>
<td align="left" width="63%">
Access to the type of firewall profile currently in effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-get_localpolicy">LocalPolicy</a>


</td>
<td align="left" width="63%">
Access to the local firewall policy.

</td>
</tr>
</table> 


## -remarks



<b>Windows Vista:  </b>Windows Vista users must use applications developed in Windows Vista for all methods and properties of this interface.

This interface is
supported by the HNetCfg.FwMgr COM object. 

All configuration changes take
effect immediately.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

