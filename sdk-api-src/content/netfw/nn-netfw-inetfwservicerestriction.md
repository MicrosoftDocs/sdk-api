---
UID: NN:netfw.INetFwServiceRestriction
title: INetFwServiceRestriction (netfw.h)
author: windows-sdk-content
description: Access to the Windows Service Hardening networking rules.
old-location: ics\inetfwservicerestriction.htm
tech.root: ics
ms.assetid: e426cae9-8c39-44cf-bd48-3b385fdfbdf7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwServiceRestriction, INetFwServiceRestriction interface [ICS/ICF], INetFwServiceRestriction interface [ICS/ICF],described, ics.inetfwservicerestriction, netfw/INetFwServiceRestriction
ms.topic: interface
f1_keywords: 
 - "netfw/INetFwServiceRestriction"
dev_langs:
 - c++
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwServiceRestriction
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwServiceRestriction interface


## -description


The <b>INetFwServiceRestriction</b> interface provides access to the Windows Service Hardening networking rules.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwServiceRestriction</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwServiceRestriction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwServiceRestriction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwservicerestriction-get_rules">get_Rules</a>
</td>
<td align="left" width="63%">
Retrieves the collection of Windows Service Hardening network rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwservicerestriction-restrictservice">RestrictService</a>
</td>
<td align="left" width="63%">
Turns service restriction on or off for a given service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwservicerestriction-servicerestricted">ServiceRestricted</a>
</td>
<td align="left" width="63%">
Queries the service restriction state of a given service.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwServiceRestriction</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwservicerestriction-get_rules">Rules</a>


</td>
<td align="left" width="63%">
Retrieves the collection of Windows Service Hardening network rules

</td>
</tr>
</table> 


## -remarks



When adding rules, note that there may be a small time lag before the newly-added rule is applied.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

