---
UID: NF:wingdi.CreateEllipticRgnIndirect
title: CreateEllipticRgnIndirect function
author: windows-sdk-content
description: The CreateEllipticRgnIndirect function creates an elliptical region.
old-location: gdi\createellipticrgnindirect.htm
tech.root: gdi
ms.assetid: bd30516e-1e05-4b7d-a6bf-7512cf3ef30f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateEllipticRgnIndirect, CreateEllipticRgnIndirect function [Windows GDI], _win32_CreateEllipticRgnIndirect, gdi.createellipticrgnindirect, wingdi/CreateEllipticRgnIndirect
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
 - CreateEllipticRgnIndirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateEllipticRgnIndirect function


## -description


The <b>CreateEllipticRgnIndirect</b> function creates an elliptical region.


## -parameters




### -param lprect [in]

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the coordinates of the upper-left and lower-right corners of the bounding rectangle of the ellipse in logical units.


## -returns



If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the <b>HRGN</b> object, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

A bounding rectangle defines the size, shape, and orientation of the region: The long sides of the rectangle define the length of the ellipse's major axis; the short sides define the length of the ellipse's minor axis; and the center of the rectangle defines the intersection of the major and minor axes.




## -see-also




<a href="https://msdn.microsoft.com/b4e9b210-8e22-42db-bb6e-65f1fb870eff">CreateEllipticRegn</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

