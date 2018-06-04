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

# IAccessibilityDockingService::DockWindow


## -description


Docks the specified window handle to the specified monitor handle.


## -parameters




### -param hwnd [in]

The accessibility application window that will be docked on the passed monitor handle.


### -param hMonitor [in]

The monitor on which the accessibility application window will be docked.


### -param cyRequested




### -param pCallback [in]

The callback pointer on which the accessibility application will receive the <a href="https://msdn.microsoft.com/8A88D02C-E542-49F0-B423-771E755D506D">Undock</a> notification.


#### - uHeight [in]

The height at which the window will be docked, in pixels, if this function is successful. Must be less than or equal to the <i>puMaxHeight</i> variable retrieved from a call to the <a href="https://msdn.microsoft.com/1C838B01-EF26-4FCC-878F-A36DEFBA3142">GetAvailableSize</a> method.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The window handle or monitor handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process is not a UIAcess accessibility application or the calling process does not own the window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMM_E_DOCKOCCUPIED</b></dt>
</dl>
</td>
<td width="60%">
There is already another window occupying the docking space. Only one window can be docked at a time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMM_E_INSUFFICIENTHEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The requested <i>uHeight</i> is larger than the maximum allowed docking height for the specified monitor. However, if this error code is being returned, it means that this monitor does support docking, though at a height indicated by a call to the <a href="https://msdn.microsoft.com/1C838B01-EF26-4FCC-878F-A36DEFBA3142">GetAvailableSize</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_MONITOR_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The monitor specified by the monitor handle does not support docking.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/DBAFE260-0AC6-4801-8590-DE058667C9A6">IAccessibilityDockingService</a>
 

 

