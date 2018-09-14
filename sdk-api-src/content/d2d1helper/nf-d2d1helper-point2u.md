---
UID: NF:d2d1helper.Point2U
title: Point2U function
author: windows-sdk-content
description: Creates a D2D1_POINT_2U structure that contains the specified x-coordinates and y-coordinates.
old-location: direct2d\point2u.htm
tech.root: Direct2D
ms.assetid: 79a19a38-3941-41bd-a1bd-5260ba36541f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Point2U, Point2U function [Direct2D], d2d1helper/Point2U, direct2d.point2u
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
 - Point2U
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Point2U function


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Dd368142(v=VS.85).aspx">D2D1_POINT_2U</a> structure that contains the specified x-coordinates and y-coordinates.


## -parameters




### -param x

Type: <b>UINT32</b>

The x-coordinate of the point. The default value is 0.


### -param y

Type: <b>UINT32</b>

The y-coordinate of the point. The default value is 0.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368142(v=VS.85).aspx">D2D1_POINT_2U</a></b>

The new point.



