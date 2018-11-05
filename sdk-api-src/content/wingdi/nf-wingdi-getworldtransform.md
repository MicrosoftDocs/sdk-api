---
UID: NF:wingdi.GetWorldTransform
title: GetWorldTransform function
author: windows-sdk-content
description: The GetWorldTransform function retrieves the current world-space to page-space transformation.
old-location: gdi\getworldtransform.htm
tech.root: gdi
ms.assetid: 72945b1e-144e-4724-bf08-6f971f8adb43
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetWorldTransform, GetWorldTransform function [Windows GDI], _win32_GetWorldTransform, gdi.getworldtransform, wingdi/GetWorldTransform
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
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetWorldTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWorldTransform function


## -description


The <b>GetWorldTransform</b> function retrieves the current world-space to page-space transformation.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpxf [out]

A pointer to an <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure that receives the current world-space to page-space transformation.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The precision of the transformation may be altered if an application calls the <a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a> function prior to calling <b>GetWorldTransform</b>. (This is because the internal format for storing transformation values uses a higher precision than a <b>FLOAT</b> value.)




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a>



<a href="https://msdn.microsoft.com/d103a4dd-949e-4f18-ac90-bb0e51011233">SetWorldTransform</a>
 

 

