---
UID: NF:d2d1helper.RectF
title: RectF function
author: windows-sdk-content
description: Creates a D2D1_RECT_F structure that contains the specified dimensions.
old-location: direct2d\rectf.htm
tech.root: Direct2D
ms.assetid: 8abcc11d-40be-45ac-9f23-b94adf9842d5
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: RectF, RectF function [Direct2D], d2d1helper/RectF, direct2d.rectf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
req.include-header: 
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
 - RectF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RectF function


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Dd368151(v=VS.85).aspx">D2D1_RECT_F</a> structure that contains the specified dimensions.


## -parameters




### -param left

Type: <b>FLOAT</b>

The x-coordinate of the upper-left corner of the rectangle. The default value is 0.f.


### -param top

Type: <b>FLOAT</b>

The y-coordinate of the upper-left corner of the rectangle. The default value is 0.f.


### -param right

Type: <b>FLOAT</b>

The x-coordinate of the lower-right corner of the rectangle. The default value is 0.f.


### -param bottom

Type: <b>FLOAT</b>

The y-coordinate of the lower-right corner of the rectangle. The default value is 0.f.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368151(v=VS.85).aspx">D2D1_RECT_F</a></b>

A rectangle structure that contains the specified dimensions.



