---
UID: NF:wingdi.CreateEllipticRgn
title: CreateEllipticRgn function
author: windows-sdk-content
description: The CreateEllipticRgn function creates an elliptical region.
old-location: gdi\createellipticrgn.htm
tech.root: gdi
ms.assetid: b4e9b210-8e22-42db-bb6e-65f1fb870eff
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateEllipticRgn, CreateEllipticRgn function [Windows GDI], _win32_CreateEllipticRgn, gdi.createellipticrgn, wingdi/CreateEllipticRgn
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
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
 - CreateEllipticRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateEllipticRgn function


## -description


The <b>CreateEllipticRgn</b> function creates an elliptical region.


## -parameters




### -param x1 [in]

Specifies the x-coordinate in logical units, of the upper-left corner of the bounding rectangle of the ellipse.


### -param y1 [in]

Specifies the y-coordinate in logical units, of the upper-left corner of the bounding rectangle of the ellipse.


### -param x2 [in]

Specifies the x-coordinate in logical units, of the lower-right corner of the bounding rectangle of the ellipse.


### -param y2 [in]

Specifies the y-coordinate in logical units, of the lower-right corner of the bounding rectangle of the ellipse.


## -returns



If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the HRGN object, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

A bounding rectangle defines the size, shape, and orientation of the region: The long sides of the rectangle define the length of the ellipse's major axis; the short sides define the length of the ellipse's minor axis; and the center of the rectangle defines the intersection of the major and minor axes.




## -see-also




<a href="https://msdn.microsoft.com/bd30516e-1e05-4b7d-a6bf-7512cf3ef30f">CreateEllipticRegnIndirect</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

