---
UID: NF:d2d1effectauthor.ID2D1Transform.MapInvalidRect
title: ID2D1Transform::MapInvalidRect
author: windows-sdk-content
description: Sets the input rectangles for this rendering pass into the transform.
old-location: direct2d\id2d1transform_setinputrects.htm
tech.root: direct2d
ms.assetid: 46E6EAF3-7EC7-4433-90E5-4C6E3A56AFA5
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1Transform interface [Direct2D],MapInvalidRect method, ID2D1Transform.MapInvalidRect, ID2D1Transform::MapInvalidRect, MapInvalidRect, MapInvalidRect method [Direct2D], MapInvalidRect method [Direct2D],ID2D1Transform interface, d2d1effectauthor/ID2D1Transform::MapInvalidRect, direct2d.id2d1transform_setinputrects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1Transform.MapInvalidRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Transform::MapInvalidRect


## -description


Sets the input rectangles for this rendering pass into the transform.


## -parameters




### -param inputIndex

Type: <b>UINT32</b>

The index of the input rectangle.


### -param invalidInputRect

Type: <b><a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a></b>

The invalid input rectangle.


### -param invalidOutputRect [out]

Type: <b><a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a>*</b>

The output rectangle to which the input rectangle must be mapped.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The transform implementation must regard <b>MapInvalidRect</b> as purely functional. The transform implementation can base the mapped input rectangle on the transform implementation's current state as specified by the encapsulating effect properties. But the transform implementation can't change its own state in response to a call to <b>MapInvalidRect</b>. Direct2D can call this method at any time and in any sequence following a call to the <a href="https://msdn.microsoft.com/8FC15A61-767C-460A-A260-9F56A41DA87F">MapInputRectsToOutputRect</a> method.





## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>



<a href="https://msdn.microsoft.com/8A0CD795-A6D8-4817-9676-58C11DDAAEBD">ID2D1Transform</a>
 

 

