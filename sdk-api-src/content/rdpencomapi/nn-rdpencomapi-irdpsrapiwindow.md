---
UID: NN:rdpencomapi.IRDPSRAPIWindow
title: IRDPSRAPIWindow
author: windows-sdk-content
description: Represents a one-to-one mapping to a sharable window.
old-location: rdp\irdpsrapiwindow.htm
old-project: rdp
ms.assetid: 85c8263b-e796-4748-b8e5-6315e5937861
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: IRDPSRAPIWindow, IRDPSRAPIWindow interface [RDP], IRDPSRAPIWindow interface [RDP],described, rdp.irdpsrapiwindow, rdpencomapi/IRDPSRAPIWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPIWindow interface


## -description


Represents a one-to-one mapping to a sharable window. A sharable window is usually a top-level window that does not have an owner. Sharing the content of a window can be enabled or disabled by setting the <a href="https://msdn.microsoft.com/e07ebdbc-79ce-4a85-9960-197c4c7ca445">Shared</a> property on the window object to <b>TRUE</b> or <b>FALSE</b>. Applications can use this window object to display a list of windows that can be shared.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIWindow</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRDPSRAPIWindow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPIWindow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b7aa5e7-7981-41c4-bb47-30b3d0d54bc1">Show</a>
</td>
<td align="left" width="63%">
Brings the current window to the foreground.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIWindow</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/jj159071">Application</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An application object that owns the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/64215325-fb94-4708-9391-5ef86c2c0076">Flags</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The flags on the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The ID of the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e07ebdbc-79ce-4a85-9960-197c4c7ca445">Shared</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The shared state of the window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/9ea90838-6de3-4b21-8db8-ff96e026505a">IRDPSRAPIWindowList</a>
 

 

