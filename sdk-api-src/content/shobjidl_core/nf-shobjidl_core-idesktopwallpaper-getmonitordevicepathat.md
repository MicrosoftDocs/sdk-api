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

# IDesktopWallpaper::GetMonitorDevicePathAt


## -description


Retrieves the unique ID of one of the system's monitors.


## -parameters




### -param monitorIndex [in]

The number of the monitor. Call <a href="https://msdn.microsoft.com/E7490E24-7BCE-4fbb-8512-998EAE045CE7">GetMonitorDevicePathCount</a> to determine the total number of monitors.


### -param monitorID [out]

A pointer to the address of a buffer that, when this method returns successfully, receives the monitor's ID.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code, including the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided in <i>monitorID</i>.

</td>
</tr>
</table>
 




## -remarks



This method can be called on monitors that are currently detached but that have an image assigned to them. Call <a href="https://msdn.microsoft.com/98A3F193-DBCF-42ec-9283-53F0F46BB1C4">GetMonitorRECT</a> to distinguish between attached and detached monitors.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/E7490E24-7BCE-4fbb-8512-998EAE045CE7">IDesktopWallpaper::GetMonitorDevicePathCount</a>
 

 

