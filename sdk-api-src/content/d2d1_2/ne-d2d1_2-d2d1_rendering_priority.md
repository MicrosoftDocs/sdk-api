---
UID: NE:d2d1_2.D2D1_RENDERING_PRIORITY
title: D2D1_RENDERING_PRIORITY
author: windows-sdk-content
description: The rendering priority affects the extent to which Direct2D will throttle its rendering workload.
old-location: direct2d\d2d1_rendering_priority.htm
tech.root: Direct2D
ms.assetid: 25DC645B-7693-468C-AE11-05F6D1B11741
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: D2D1_RENDERING_PRIORITY, D2D1_RENDERING_PRIORITY enumeration [Direct2D], D2D1_RENDERING_PRIORITY_LOW, D2D1_RENDERING_PRIORITY_NORMAL, d2d1_2/D2D1_RENDERING_PRIORITY, d2d1_2/D2D1_RENDERING_PRIORITY_LOW, d2d1_2/D2D1_RENDERING_PRIORITY_NORMAL, direct2d.d2d1_rendering_priority
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - D2D1_2.h
api_name:
 - D2D1_RENDERING_PRIORITY
product: Windows
targetos: Windows
req.typenames: D2D1_RENDERING_PRIORITY
req.redist: 
---

# D2D1_RENDERING_PRIORITY enumeration


## -description


The rendering priority affects the extent to which <a href="https://msdn.microsoft.com/en-us/library/Dd370990(v=VS.85).aspx">Direct2D</a> will throttle its rendering workload.


## -enum-fields




### -field D2D1_RENDERING_PRIORITY_NORMAL

No change in rendering workload priority.


### -field D2D1_RENDERING_PRIORITY_LOW

The device and its associated device contexts are given a lower priority than others.


### -field D2D1_RENDERING_PRIORITY_FORCE_DWORD



