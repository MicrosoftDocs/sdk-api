---
UID: NF:wingdi.CombineTransform
title: CombineTransform function
author: windows-driver-content
description: The CombineTransform function concatenates two world-space to page-space transformations.
old-location: gdi\combinetransform.htm
old-project: gdi
ms.assetid: 6ccd7828-7aa6-4c86-a340-b93e50cf3a2a
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CombineTransform, CombineTransform function [Windows GDI], _win32_CombineTransform, gdi.combinetransform, wingdi/CombineTransform
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	CombineTransform
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CombineTransform function


## -description


The <b>CombineTransform</b> function concatenates two world-space to page-space transformations.


## -parameters




### -param lpxfOut

TBD


### -param lpxf1

TBD


### -param lpxf2

TBD




#### - lpxform1 [in]

A pointer to an <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure that specifies the first transformation.


#### - lpxform2 [in]

A pointer to an <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure that specifies the second transformation.


#### - lpxformResult [out]

A pointer to an <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure that receives the combined transformation.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Applying the combined transformation has the same effect as applying the first transformation and then applying the second transformation.

The three transformations need not be distinct. For example, <i>lpxform1</i> can point to the same <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure as <i>lpxformResult</i>.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/72945b1e-144e-4724-bf08-6f971f8adb43">GetWorldTransform</a>



<a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a>



<a href="https://msdn.microsoft.com/d103a4dd-949e-4f18-ac90-bb0e51011233">SetWorldTransform</a>



<a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a>
 

 

