---
UID: NE:d2d1_1.D2D1_MAP_OPTIONS
title: D2D1_MAP_OPTIONS
author: windows-sdk-content
description: Specifies how the memory to be mapped from the corresponding ID2D1Bitmap1 should be treated.
old-location: direct2d\__d2d1_map_options.htm
tech.root: direct2d
ms.assetid: 8706c3e3-eb29-4760-bdfd-f19afc6f2bf7
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: D2D1_MAP_OPTIONS, D2D1_MAP_OPTIONS enumeration [Direct2D], D2D1_MAP_OPTIONS_DISCARD, D2D1_MAP_OPTIONS_READ, D2D1_MAP_OPTIONS_WRITE, d2d1_1/D2D1_MAP_OPTIONS, d2d1_1/D2D1_MAP_OPTIONS_DISCARD, d2d1_1/D2D1_MAP_OPTIONS_READ, d2d1_1/D2D1_MAP_OPTIONS_WRITE, direct2d.__d2d1_map_options
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
 - D2d1_1.h
api_name:
 - D2D1_MAP_OPTIONS
product: Windows
targetos: Windows
req.typenames: D2D1_MAP_OPTIONS
req.redist: 
---

# D2D1_MAP_OPTIONS enumeration


## -description


Specifies how the memory to be mapped from the corresponding <a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a> should be treated.


## -enum-fields




### -field D2D1_MAP_OPTIONS_NONE


### -field D2D1_MAP_OPTIONS_READ

Allow CPU Read access.


### -field D2D1_MAP_OPTIONS_WRITE

Allow CPU Write access.


### -field D2D1_MAP_OPTIONS_DISCARD

Discard the previous contents of the resource when it is mapped.


### -field D2D1_MAP_OPTIONS_FORCE_DWORD




## -remarks



The <b>D2D1_MAP_OPTIONS_READ</b> option can be used only if the bitmap was created with the <b>D2D1_BITMAP_OPTIONS_CPU_READ</b> flag.

These flags will be not be able to be used on bitmaps created by the <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>. However, the ID2D1SourceTransform will receive bitmaps for which these flags are valid.

<b>D2D1_MAP_OPTIONS_DISCARD</b> can only be used with <b>D2D1_MAP_OPTIONS_WRITE</b>.  Both of these options are only available through the effect author API, not through the Direct2D rendering API.





## -see-also




<a href="https://msdn.microsoft.com/284c16ea-1a9f-4f13-b359-214178650add">ID2D1Bitmap1::Map</a>
 

 

