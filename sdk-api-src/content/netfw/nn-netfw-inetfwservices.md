---
UID: NN:netfw.INetFwServices
title: INetFwServices (netfw.h)
description: The INetFwServices interface is a standard Automation interface which provides access to a collection of services that may be authorized to listen through the firewall.
old-location: ics\inetfwservices.htm
tech.root: ics
ms.assetid: b99464c5-dabc-405a-ad3e-da06a6faef47
ms.date: 12/05/2018
ms.keywords: INetFwServices, INetFwServices interface [ICS/ICF], INetFwServices interface [ICS/ICF],described, ics.inetfwservices, netfw/INetFwServices
f1_keywords:
- netfw/INetFwServices
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
- INetFwServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwServices interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwServices</b> interface is a standard Automation interface which provides access to a collection of services that may be authorized to listen
through the firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwServices</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwservices-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwservices-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Count property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwservices-item">Item</a>
</td>
<td align="left" width="63%">
Returns the specified port if present in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwServices</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwservices-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Gets an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwservices-get_count">Count</a>


</td>
<td align="left" width="63%">
Gets the count for the collection.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is retrieved through the
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_services">Services</a> property of the INetFwProfile interface. 

All configuration
changes take effect immediately.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_services">INetFwProfile.Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

