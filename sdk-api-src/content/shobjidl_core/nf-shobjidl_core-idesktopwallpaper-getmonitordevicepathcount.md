---
UID: NF:shobjidl_core.IDesktopWallpaper.GetMonitorDevicePathCount
title: IDesktopWallpaper::GetMonitorDevicePathCount
author: windows-driver-content
description: Retrieves the number of monitors that are associated with the system.
old-location: shell\IDesktopWallpaper_GetMonitorDevicePathCount.htm
old-project: shell
ms.assetid: E7490E24-7BCE-4fbb-8512-998EAE045CE7
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetMonitorDevicePathCount, GetMonitorDevicePathCount method [Windows Shell], GetMonitorDevicePathCount method [Windows Shell],IDesktopWallpaper interface, IDesktopWallpaper interface [Windows Shell],GetMonitorDevicePathCount method, IDesktopWallpaper.GetMonitorDevicePathCount, IDesktopWallpaper::GetMonitorDevicePathCount, shell.IDesktopWallpaper_GetMonitorDevicePathCount, shobjidl_core/IDesktopWallpaper::GetMonitorDevicePathCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IDesktopWallpaper.GetMonitorDevicePathCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDesktopWallpaper::GetMonitorDevicePathCount


## -description


Retrieves the number of monitors that are associated with the system.


## -parameters




### -param count [out]

A pointer to a value that, when this method returns successfully, receives the number of monitors.


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



The count retrieved through this method includes monitors that are currently detached but that have an image assigned to them. Call <a href="https://msdn.microsoft.com/98A3F193-DBCF-42ec-9283-53F0F46BB1C4">GetMonitorRECT</a> to distinguish between attached and detached monitors.




## -see-also




<a href="https://msdn.microsoft.com/A83903B5-314B-4a8b-8D37-F8A8995DE0CB">IDesktopWallpaper</a>



<a href="https://msdn.microsoft.com/CE0C6B07-F9D1-4221-9D9D-8D17CF6780E6">IDesktopWallpaper::GetMonitorDevicePathAt</a>
 

 

