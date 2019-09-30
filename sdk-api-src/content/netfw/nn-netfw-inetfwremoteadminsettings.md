---
UID: NN:netfw.INetFwRemoteAdminSettings
title: INetFwRemoteAdminSettings (netfw.h)
author: windows-sdk-content
description: The INetFwRemoteAdminSettings interface provides access to the settings that control remote administration.
old-location: ics\inetfwremoteadminsettings.htm
tech.root: ics
ms.assetid: 35f34a53-e73b-48be-ac79-9b7ab825c6ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwRemoteAdminSettings, INetFwRemoteAdminSettings interface [ICS/ICF], INetFwRemoteAdminSettings interface [ICS/ICF],described, ics.inetfwremoteadminsettings, netfw/INetFwRemoteAdminSettings
ms.topic: interface
f1_keywords: 
 - "netfw/INetFwRemoteAdminSettings"
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
 - INetFwRemoteAdminSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwRemoteAdminSettings interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwRemoteAdminSettings</b> interface provides access to the settings that control remote administration. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRemoteAdminSettings</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwRemoteAdminSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwRemoteAdminSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_enabled">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_ipversion">get_IpVersion</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_remoteaddresses">get_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_scope">get_Scope</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Scope property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_enabled">put_Enabled</a>
</td>
<td align="left" width="63%">
Modifies the contents of the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_ipversion">put_IpVersion</a>
</td>
<td align="left" width="63%">
Modifies the contents of the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_remoteaddresses">put_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Modifies the contents of the RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_scope">put_Scope</a>
</td>
<td align="left" width="63%">
Modifies the contents of the Scope property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRemoteAdminSettings</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_enabled">Enabled</a>


</td>
<td align="left" width="63%">
Accesses the contents of the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_ipversion">IpVersion</a>


</td>
<td align="left" width="63%">
Accesses the contents of the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_remoteaddresses">RemoteAddresses</a>


</td>
<td align="left" width="63%">
Accesses the contents of the RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_scope">Scope</a>


</td>
<td align="left" width="63%">
Accesses the contents of the Scope property.

</td>
</tr>
</table> 


## -remarks



An
instance of this interface is retrieved through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_remoteadminsettings">RemoteAdminSettings</a>property of the INetFwProfile interface. 

All configuration changes take
 effect immediately.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

