---
UID: NF:wingdi.PtVisible
title: PtVisible function
author: windows-sdk-content
description: The PtVisible function determines whether the specified point is within the clipping region of a device context.
old-location: gdi\ptvisible.htm
old-project: gdi
ms.assetid: 72ccbd0f-f85b-434d-b0fc-dbe26348a74d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: PtVisible, PtVisible function [Windows GDI], _win32_PtVisible, gdi.ptvisible, wingdi/PtVisible
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - PtVisible
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PtVisible function


## -description


The <b>PtVisible</b> function determines whether the specified point is within the clipping region of a device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x

TBD


### -param y

TBD




#### - X [in]

The x-coordinate, in logical units, of the point.


#### - Y [in]

The y-coordinate, in logical units, of the point.


## -returns



If the specified point is within the clipping region of the device context, the return value is <b>TRUE</b>(1).

If the specified point is not within the clipping region of the device context, the return value is <b>FALSE</b>(0).

If the <b>HDC</b> is not valid, the return value is (BOOL)-1.




## -see-also




<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/990e9b22-0ce3-42b8-a87e-32fd2f2bc2fb">RectVisible</a>
 

 

