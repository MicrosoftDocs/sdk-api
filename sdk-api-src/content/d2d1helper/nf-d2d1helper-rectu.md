---
UID: NF:d2d1helper.RectU
title: RectU function
author: windows-sdk-content
description: Creates a D2D1_RECT_U structure that contains the specified dimensions.
old-location: direct2d\rectu.htm
old-project: Direct2D
ms.assetid: a0b7b850-b58d-43a0-b5c5-61a3791f0681
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: RectU, RectU function [Direct2D], d2d1helper/RectU, direct2d.rectu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D2d1.dll
api_name:
-	RectU
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# RectU function


## -description


Creates a <a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a> structure that contains the specified dimensions.


## -parameters




### -param left

Type: <b>UINT32</b>

The x-coordinate of the upper-left corner of the rectangle. The default value is 0.


### -param top

Type: <b>UINT32</b>

The y-coordinate of the upper-left corner of the rectangle. The default value is 0.


### -param right

Type: <b>UINT32</b>

The x-coordinate of the lower-right corner of the rectangle. The default value is 0.


### -param bottom

Type: <b>UINT32</b>

The y-coordinate of the lower-right corner of the rectangle. The default value is 0.


## -returns



Type: <b><a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a></b>

A rectangle structure that contains the specified dimensions.



