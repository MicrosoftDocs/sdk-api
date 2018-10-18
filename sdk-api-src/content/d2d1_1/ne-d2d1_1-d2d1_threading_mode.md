---
UID: NE:d2d1_1.D2D1_THREADING_MODE
title: D2D1_THREADING_MODE
author: windows-sdk-content
description: Specifies the threading mode used while simultaneously creating the device, factory, and device context.
old-location: direct2d\__d2d1_threading_mode.htm
tech.root: direct2d
ms.assetid: 21fba5ee-3d31-4142-b66a-94b343e1c6eb
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: D2D1_THREADING_MODE, D2D1_THREADING_MODE enumeration [Direct2D], D2D1_THREADING_MODE_MULTI_THREADED, D2D1_THREADING_MODE_SINGLE_THREADED, d2d1_1/D2D1_THREADING_MODE, d2d1_1/D2D1_THREADING_MODE_MULTI_THREADED, d2d1_1/D2D1_THREADING_MODE_SINGLE_THREADED, direct2d.__d2d1_threading_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - d2d1_1.h
api_name:
 - D2D1_THREADING_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_THREADING_MODE
req.redist: 
---

# D2D1_THREADING_MODE enumeration


## -description


Specifies the threading mode used while simultaneously creating the device, factory, and device context.



## -enum-fields




### -field D2D1_THREADING_MODE_SINGLE_THREADED

Resources may only be invoked serially.  Device context state is not protected from multi-threaded access. 


### -field D2D1_THREADING_MODE_MULTI_THREADED

Resources may be invoked from multiple threads. Resources use interlocked reference counting and their state is protected.



### -field D2D1_THREADING_MODE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404298(v=VS.85).aspx">D2D1_CREATION_PROPERTIES</a>



<a href="https://msdn.microsoft.com/en-us/library/JJ569217(v=VS.85).aspx">Multithreaded Direct2D Apps</a>
 

 

