---
UID: NF:d2d1effectauthor.ID2D1Transform.MapOutputRectToInputRects
title: ID2D1Transform::MapOutputRectToInputRects
author: windows-sdk-content
description: Allows a transform to state how it would map a rectangle requested on its output to a set of sample rectangles on its input.
old-location: direct2d\id2d1transform_mapoutputrecttoinputrects.htm
tech.root: Direct2D
ms.assetid: EE098F67-B5A7-41C1-886A-2C7779B5E05C
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ID2D1Transform interface [Direct2D],MapOutputRectToInputRects method, ID2D1Transform.MapOutputRectToInputRects, ID2D1Transform::MapOutputRectToInputRects, MapOutputRectToInputRects, MapOutputRectToInputRects method [Direct2D], MapOutputRectToInputRects method [Direct2D],ID2D1Transform interface, d2d1effectauthor/ID2D1Transform::MapOutputRectToInputRects, direct2d.id2d1transform_mapoutputrecttoinputrects
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
 - ID2D1Transform.MapOutputRectToInputRects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Transform::MapOutputRectToInputRects


## -description


Allows a transform to state how it would map a rectangle requested on its output to a set of sample rectangles on its input.


## -parameters




### -param outputRect

Type: <b>const <a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a>*</b>

The output rectangle from which the inputs must be mapped.


### -param inputRects [out]

Type: <b><a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a>*</b>

The corresponding set of inputs. The inputs will directly correspond to the transform inputs.


### -param inputRectsCount

Type: <b>UINT32</b>

The number of inputs specified. <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> guarantees that this is equal to the number of inputs specified on the transform.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The transform implementation must ensure that any pixel shader or software callback implementation it provides honors this calculation.

The transform implementation must regard this method as purely functional. It can base the mapped input and output rectangles on its current state as specified by the encapsulating effect properties.    However, it must not change its own state in response to this method being invoked. The <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> renderer implementation reserves the right to call this method at any time and in any sequence.




## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>



<a href="https://msdn.microsoft.com/8A0CD795-A6D8-4817-9676-58C11DDAAEBD">ID2D1Transform</a>
 

 

