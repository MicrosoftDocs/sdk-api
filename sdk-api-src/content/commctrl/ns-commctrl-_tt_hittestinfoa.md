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

# _TT_HITTESTINFOA structure


## -description


Contains information that a tooltip control uses to determine whether a point is in the bounding rectangle of the specified tool. If the point is in the rectangle, the structure receives information about the tool. 


## -struct-fields




### -field hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tool or window with the specified tool. 


### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

Client coordinates of the point to test. 


### -field ti

Type: <b><a href="https://msdn.microsoft.com/82ca63f3-b99d-4371-877a-f96ed2ad8f34">TOOLINFO</a></b>


<a href="https://msdn.microsoft.com/82ca63f3-b99d-4371-877a-f96ed2ad8f34">TOOLINFO</a> structure. If the point specified by 
					<b>pt</b> is in the tool specified by 
					<b>hwnd</b>, this structure receives information about the tool. The 
					<b>cbSize</b> member of this structure must be filled in before sending this message. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/d4dcc29b-c64c-41b8-a153-300df68ecdf5">TTM_HITTEST</a> message. 



