---
UID: NF:d2d1helper.RoundedRect
title: RoundedRect function
author: windows-sdk-content
description: Creates a D2D1_ROUNDED_RECT structure.
old-location: direct2d\roundedrect.htm
old-project: direct2d
ms.assetid: 200119a2-941c-493f-9e56-c9f306dc5322
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RoundedRect, RoundedRect function [Direct2D], d2d1helper/RoundedRect, direct2d.roundedrect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - RoundedRect
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# RoundedRect function


## -description


Creates a <a href="https://msdn.microsoft.com/7069ca65-170e-42fc-8c1a-849a2f25c36f">D2D1_ROUNDED_RECT</a> structure.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The size and position of the rectangle.


### -param radiusX

Type: <b>FLOAT</b>

The x-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.




### -param radiusY

Type: <b>FLOAT</b>

The y-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.




## -returns



Type: <b><a href="https://msdn.microsoft.com/7069ca65-170e-42fc-8c1a-849a2f25c36f">D2D1_ROUNDED_RECT</a></b>

The new rounded rectangle.



