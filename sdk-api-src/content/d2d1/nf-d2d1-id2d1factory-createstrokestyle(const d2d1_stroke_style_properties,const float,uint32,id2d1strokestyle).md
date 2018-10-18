---
UID: NF:d2d1.ID2D1Factory.CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES,const FLOAT,UINT32,ID2D1StrokeStyle)
title: ID2D1Factory::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES,const FLOAT,UINT32,ID2D1StrokeStyle)
author: windows-sdk-content
description: Creates an ID2D1StrokeStyle that describes start cap, dash pattern, and other features of a stroke.
old-location: direct2d\ID2D1Factory_CreateStrokeStyle_ptr_D2D1_STROKE_STYLE_PROPERTIES_ptr_FLOAT_ptr_ptr_ID2D1StrokeStyle.htm
tech.root: direct2d
ms.assetid: 17e8cd4c-6ba4-49d4-a883-2937ff2121d3
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CreateStrokeStyle, CreateStrokeStyle method [Direct2D], CreateStrokeStyle method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateStrokeStyle method, ID2D1Factory.CreateStrokeStyle, ID2D1Factory.CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES,const FLOAT,UINT32,ID2D1StrokeStyle), ID2D1Factory::CreateStrokeStyle, ID2D1Factory::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES,const FLOAT,UINT32,ID2D1StrokeStyle), d2d1/ID2D1Factory::CreateStrokeStyle, direct2d.ID2D1Factory_CreateStrokeStyle_ptr_D2D1_STROKE_STYLE_PROPERTIES_ptr_FLOAT_ptr_ptr_ID2D1StrokeStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.CreateStrokeStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES,const FLOAT,UINT32,ID2D1StrokeStyle)


## -description


Creates an <a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a> that describes start cap, dash pattern, and other features of a stroke.


## -parameters




### -param strokeStyleProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/67f3701f-febd-4afe-803e-c5d9dbcd1b21">D2D1_STROKE_STYLE_PROPERTIES</a>*</b>

A structure that describes the stroke's line cap, dash offset, and other details of a stroke.


### -param dashes [in, optional]

Type: <b>const FLOAT*</b>

An array whose elements are set to the length of each dash and space in the dash pattern. The first element sets the length of a dash, the second element sets the length of a space, the third element sets the length of a dash, and so on. The length of each dash and space in the dash pattern is the product of the element value in the array and the stroke width. 


### -param dashesCount

Type: <b>UINT</b>

The number of elements in the <i>dashes</i> array. 


### -param strokeStyle [out]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>**</b>

When this method returns, contains the address of the pointer to the stroke style created by this method.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

