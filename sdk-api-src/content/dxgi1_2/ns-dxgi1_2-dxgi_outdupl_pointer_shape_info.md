---
UID: NS:dxgi1_2.DXGI_OUTDUPL_POINTER_SHAPE_INFO
title: DXGI_OUTDUPL_POINTER_SHAPE_INFO
author: windows-sdk-content
description: The DXGI_OUTDUPL_POINTER_SHAPE_INFO structure describes information about the cursor shape.
old-location: direct3ddxgi\dxgi_outdupl_pointer_shape_info.htm
old-project: direct3ddxgi
ms.assetid: 8C270C30-01B8-467C-939F-7F4B82B9ED15
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DXGI_OUTDUPL_POINTER_SHAPE_INFO, DXGI_OUTDUPL_POINTER_SHAPE_INFO structure [DXGI], direct3ddxgi.dxgi_outdupl_pointer_shape_info, dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXGI_OUTDUPL_POINTER_SHAPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DXGI1_2.h
api_name:
-	DXGI_OUTDUPL_POINTER_SHAPE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_OUTDUPL_POINTER_SHAPE_INFO structure


## -description


The <b>DXGI_OUTDUPL_POINTER_SHAPE_INFO</b> structure describes information about the cursor shape.


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/A066B6D3-A72A-48A9-BAED-BC3488BD1BC7">DXGI_OUTDUPL_POINTER_SHAPE_TYPE</a>-typed value that specifies the type of cursor shape. 


### -field Width

The width in pixels of the mouse cursor.


### -field Height

The height in scan lines of the mouse cursor.


### -field Pitch

The width in bytes of the mouse cursor.


### -field HotSpot

The position of the cursor's hot spot relative to its upper-left pixel. An application does not use the hot spot when it determines where to draw the cursor shape.


## -remarks



An application draws the cursor shape with the top-left-hand corner drawn at the position that the <b>Position</b> member of the  <a href="https://msdn.microsoft.com/CCD55021-8F67-463D-BA00-46D8B9D22B9A">DXGI_OUTDUPL_POINTER_POSITION</a> structure specifies; the application does not use the hot spot to draw the cursor shape.

An application calls the  <a href="https://msdn.microsoft.com/321FDB62-BF0E-402E-A00B-6F60B7F132AA">IDXGIOutputDuplication::GetFramePointerShape</a> method to retrieve cursor shape information in a  <b>DXGI_OUTDUPL_POINTER_SHAPE_INFO</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/321FDB62-BF0E-402E-A00B-6F60B7F132AA">IDXGIOutputDuplication::GetFramePointerShape</a>
 

 

