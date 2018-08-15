---
UID: NF:wingdi.RectVisible
title: RectVisible function
author: windows-sdk-content
description: The RectVisible function determines whether any part of the specified rectangle lies within the clipping region of a device context.
old-location: gdi\rectvisible.htm
old-project: gdi
ms.assetid: 990e9b22-0ce3-42b8-a87e-32fd2f2bc2fb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RectVisible, RectVisible function [Windows GDI], _win32_RectVisible, gdi.rectvisible, wingdi/RectVisible
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.redist: 
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
 - ext-ms-win-gdi-clipping-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - RectVisible
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# RectVisible function


## -description


The <b>RectVisible</b> function determines whether any part of the specified rectangle lies within the clipping region of a device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lprect [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the logical coordinates of the specified rectangle.


## -returns



If the current transform does not have a rotation and the rectangle lies within the clipping region, the return value is <b>TRUE</b> (1).

If the current transform does not have a rotation and the rectangle does not lie within the clipping region, the return value is <b>FALSE</b> (0).

If the current transform has a rotation and the rectangle lies within the clipping region, the return value is 2.

If the current transform has a rotation and the rectangle does not lie within the clipping region, the return value is 1.

All other return values are considered error codes. If the any parameter is not valid, the return value is undefined.




## -see-also




<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/72ccbd0f-f85b-434d-b0fc-dbe26348a74d">PtVisible</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/7a4f0b9c-8588-4da8-a030-ed9d8b4ee08d">SelectClipRgn</a>
 

 

