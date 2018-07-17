---
UID: NN:netfw.INetFwServiceRestriction
title: INetFwServiceRestriction
author: windows-sdk-content
description: Access to the Windows Service Hardening networking rules.
old-location: ics\inetfwservicerestriction.htm
old-project: ics
ms.assetid: e426cae9-8c39-44cf-bd48-3b385fdfbdf7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: INetFwServiceRestriction, INetFwServiceRestriction interface [ICS/ICF], INetFwServiceRestriction interface [ICS/ICF],described, ics.inetfwservicerestriction, netfw/INetFwServiceRestriction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwServiceRestriction
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwServiceRestriction interface


## -description


The <b>INetFwServiceRestriction</b> interface provides access to the Windows Service Hardening networking rules.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwServiceRestriction</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetFwServiceRestriction</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12846607-daf7-43ce-8278-89db15b95a81">get_Rules</a>
</td>
<td align="left" width="63%">
Retrieves the collection of Windows Service Hardening network rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5695bcb7-a83a-4581-8f46-00e85273b160">RestrictService</a>
</td>
<td align="left" width="63%">
Turns service restriction on or off for a given service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38fe5a68-44ab-4bcb-8673-ebb1e87e446f">ServiceRestricted</a>
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

<a href="https://msdn.microsoft.com/12846607-daf7-43ce-8278-89db15b95a81">Rules</a>


</td>
<td align="left" width="63%">
Retrieves the collection of Windows Service Hardening network rules

</td>
</tr>
</table> 


## -remarks



When adding rules, note that there may be a small time lag before the newly-added rule is applied.




## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

