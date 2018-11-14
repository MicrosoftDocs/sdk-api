---
UID: NN:shobjidl.IAccessibilityDockingService
title: IAccessibilityDockingService
author: windows-sdk-content
description: Docks an application window to the bottom of a monitor when a Windows Store app is visible and not snapped, or when the launcher is visible.
old-location: com\iaccessibilitydockingservice.htm
tech.root: com
ms.assetid: DBAFE260-0AC6-4801-8590-DE058667C9A6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAccessibilityDockingService, IAccessibilityDockingService interface [COM], IAccessibilityDockingService interface [COM],described, com.iaccessibilitydockingservice, shobjidl/IAccessibilityDockingService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl.h
api_name:
 - IAccessibilityDockingService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibilityDockingService interface


## -description


Docks an application window to the bottom of a monitor when a Windows Store app is visible and not snapped, or when the launcher is visible.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibilityDockingService</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IAccessibilityDockingService</b> also has these types of members:
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

