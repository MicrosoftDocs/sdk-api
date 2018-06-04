---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAccessibilityDockingService interface


## -description


Docks an application window to the bottom of a monitor when a Windows Store app is visible and not snapped, or when the launcher is visible.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibilityDockingService</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IAccessibilityDockingService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibilityDockingService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99C6A82C-A421-4A5E-B23A-167384A7AB90">DockWindow</a>
</td>
<td align="left" width="63%">
Docks the specified window handle to the specified monitor handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1C838B01-EF26-4FCC-878F-A36DEFBA3142">GetAvailableSize</a>
</td>
<td align="left" width="63%">
Gets the dimensions available for docking an accessibility window on a monitor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8A88D02C-E542-49F0-B423-771E755D506D">UnDockWindow</a>
</td>
<td align="left" width="63%">
Undocks the specified window handle if it is currently docked.

</td>
</tr>
</table> 

