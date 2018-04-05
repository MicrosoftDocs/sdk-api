---
UID: NS:d3d9types._D3DRESOURCESTATS
title: "_D3DRESOURCESTATS"
author: windows-driver-content
description: Resource statistics gathered by the D3DDEVINFO_ResourceManager when using the asynchronous query mechanism.
old-location: direct3d9\d3dresourcestats.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dresourcestats.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 31574d0d-0e93-7e2f-e89e-bc8d82860921, D3DRESOURCESTATS, D3DRESOURCESTATS structure [Direct3D 9], LPD3DRESOURCESTATS, LPD3DRESOURCESTATS structure pointer [Direct3D 9], _D3DRESOURCESTATS, d3d9types/D3DRESOURCESTATS, d3d9types/LPD3DRESOURCESTATS, direct3d9.d3dresourcestats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DRESOURCESTATS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DRESOURCESTATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DRESOURCESTATS structure


## -description


Resource statistics gathered by the <a href="https://msdn.microsoft.com/e43de550-2025-4210-a420-e41d14620704">D3DDEVINFO_ResourceManager</a> when using the asynchronous query mechanism.


## -struct-fields




### -field bThrashing

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Indicates if thrashing is occurring.


### -field ApproxBytesDownloaded

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Approximate number of bytes downloaded by the resource manager.


### -field NumEvicts

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Number of objects evicted.


### -field NumVidCreates

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Number of objects created in video memory.


### -field LastPri

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Priority of last object evicted.


### -field NumUsed

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Number of objects set to the device.


### -field NumUsedInVidMem

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Number of objects set to the device, which are already in video memory.


### -field WorkingSet

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Number of objects in video memory.


### -field WorkingSetBytes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Number of bytes in video memory.


### -field TotalManaged

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Total number of managed objects.


### -field TotalBytes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Total number of bytes of managed objects.


## -see-also




<a href="https://msdn.microsoft.com/81e1c5c5-03bc-4598-814e-14e56513e221">Asynchronous Notification (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

