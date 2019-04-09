---
UID: NN:netfw.INetFwPolicy
title: INetFwPolicy (netfw.h)
author: windows-sdk-content
description: The INetFwPolicy interface provides access to a firewall policy.
old-location: ics\inetfwpolicy.htm
tech.root: ics
ms.assetid: 8bfe55b6-c38d-47f8-9160-a304a85eb67f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwPolicy, INetFwPolicy interface [ICS/ICF], INetFwPolicy interface [ICS/ICF],described, ics.inetfwpolicy, netfw/INetFwPolicy
ms.topic: interface
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
 - INetFwPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwPolicy interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwPolicy</b> interface  provides access to a firewall policy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwPolicy</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetFwPolicy</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2ee59a3e-a4e3-4714-aba7-9d72bfacfb34">get_CurrentProfile</a>
</td>
<td align="left" width="63%">
Retrieves the current profile in effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c3876cf-40a4-4315-a87a-8fcdf509d48e">GetProfileByType</a>
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

<a href="https://msdn.microsoft.com/fa6d79a8-37e4-4172-a6be-3ca803c0feca">CurrentProfile</a>


</td>
<td align="left" width="63%">
Access to the type of firewall profile currently in effect.

</td>
</tr>
</table> 


## -remarks



Instances of this interface are
retrieved through the <a href="https://msdn.microsoft.com/ec32c591-d677-4251-90c8-1bd4fa516245">LocalPolicy</a> property of the <a href="https://msdn.microsoft.com/7534ea10-7553-4ec2-af68-0b0393ffc003">INetFwMgr</a> interface.

All configuration changes take
effect immediately.

The Windows Firewall/Internet Connection Sharing  service must be running to access this interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/7534ea10-7553-4ec2-af68-0b0393ffc003">INetFwMgr</a>



<a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

