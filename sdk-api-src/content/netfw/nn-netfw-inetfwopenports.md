---
UID: NN:netfw.INetFwOpenPorts
title: INetFwOpenPorts
author: windows-sdk-content
description: The INetFwOpenPorts interface is a standard Automation collection interface.
old-location: ics\inetfwopenports.htm
tech.root: ICS
ms.assetid: a3a6e5c1-5818-419c-8df4-966b2fbcd8c0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: INetFwOpenPorts, INetFwOpenPorts interface [ICS/ICF], INetFwOpenPorts interface [ICS/ICF],described, ics.inetfwopenports, netfw/INetFwOpenPorts
ms.prod: windows
ms.technology: windows-sdk
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
 - INetFwOpenPorts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwOpenPorts interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwOpenPorts</b> interface is a standard Automation collection interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwOpenPorts</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetFwOpenPorts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwOpenPorts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd97333d-9bd5-4ab2-9189-75a7f7f52622">Add</a>
</td>
<td align="left" width="63%">
Opens a new port and adds it to  the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7de2fef-7966-4742-a821-7fce0bf3bba2">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83d95b38-0c0d-4325-904e-7953ccef24e7">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Count property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0491047-d20d-49e4-9319-421b48feca48">Item</a>
</td>
<td align="left" width="63%">
Returns the specified port if present in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3719087-f7b9-4780-a030-0c568248080d">Remove</a>
</td>
<td align="left" width="63%">
Closes a port and removes it from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwOpenPorts</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a7de2fef-7966-4742-a821-7fce0bf3bba2">_NewEnum</a>


</td>
<td align="left" width="63%">
Gets an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/83d95b38-0c0d-4325-904e-7953ccef24e7">Count</a>


</td>
<td align="left" width="63%">
Gets the count for the collection.

</td>
</tr>
</table> 


## -remarks



An instance
of this interface is retrieved through the <a href="https://msdn.microsoft.com/9bb27bb1-7185-4b9a-a529-383e052e5016">GloballyOpenPorts</a> property of the
INetFwProfile interface.

All configuration changes take effect
immediately.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/1a9fd676-b1c0-4be5-9571-d14ac5980af5">INetFwOpenPort</a>



<a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>



<a href="https://msdn.microsoft.com/57a777a4-03f5-416a-ae28-474d8794a759">INetFwService</a>



<a href="_com_iunknown">IUnknown</a>
 

 

