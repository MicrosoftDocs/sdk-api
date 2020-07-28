---
UID: NN:netfw.INetFwAuthorizedApplications
title: INetFwAuthorizedApplications (netfw.h)
description: The INetFwAuthorizedApplications interface provides access to a collection of applications authorized open ports in the firewall.
helpviewer_keywords: ["INetFwAuthorizedApplications","INetFwAuthorizedApplications interface [ICS/ICF]","INetFwAuthorizedApplications interface [ICS/ICF]","described","ics.inetfwauthorizedapplications","netfw/INetFwAuthorizedApplications"]
old-location: ics\inetfwauthorizedapplications.htm
tech.root: ics
ms.assetid: 70ea2cd1-5422-4db1-ab84-9924dab5623d
ms.date: 12/05/2018
ms.keywords: INetFwAuthorizedApplications, INetFwAuthorizedApplications interface [ICS/ICF], INetFwAuthorizedApplications interface [ICS/ICF],described, ics.inetfwauthorizedapplications, netfw/INetFwAuthorizedApplications
f1_keywords:
- netfw/INetFwAuthorizedApplications
dev_langs:
- c++
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
- INetFwAuthorizedApplications
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwAuthorizedApplications interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwAuthorizedApplications</b> interface provides access to a collection of applications authorized open ports in the
firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwAuthorizedApplications</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwAuthorizedApplications</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwAuthorizedApplications</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplications-add">Add</a>
</td>
<td align="left" width="63%">
Adds a new application  to  the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplications-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplications-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Count property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplications-item">Item</a>
</td>
<td align="left" width="63%">
Returns the specified application if present in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplications-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an application  from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwAuthorizedApplications</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplications-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Gets an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplications-get_count">Count</a>


</td>
<td align="left" width="63%">
Gets the count for the collection.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is retrieved through the
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_authorizedapplications">AuthorizedApplications</a> property of the INetFwProfile interface. 

All
configuration changes take effect immediately.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_authorizedapplications">INetFwProfile.AuthorizedApplications</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

