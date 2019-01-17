---
UID: NF:d2d1_1helper.RectL
title: RectL function
author: windows-sdk-content
description: Returns a filled D2D1_RECT_L structure.
old-location: direct2d\rectl.htm
tech.root: Direct2D
ms.assetid: CE2B4034-24BC-49AE-88C6-C60BDCEA38B5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RectL, RectL function [Direct2D], dciddi/RectL, direct2d.rectl
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: D2d1_1helper.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - RectL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RectL function


## -description


Returns a filled D2D1_RECT_L structure.


## -parameters




### -param left

Type: <b>INT32</b>

The x-coordinate of the upper-left corner of the rectangle.


### -param top

Type: <b>INT32</b>

The y-coordinate of the upper-left corner of the rectangle.


### -param right

Type: <b>INT32</b>

The x-coordinate of the lower-right corner of the rectangle.


### -param bottom

Type: <b>INT32</b>

The y-coordinate of the lower-right corner of the rectangle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a></b>

The RECT structure defines the coordinates of the upper-left and lower-right corners of a rectangle.



