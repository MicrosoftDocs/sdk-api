---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle)
title: ID2D1DeviceContext2::CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle) (d2d1_3.h)
author: windows-sdk-content
description: Creates a new ID2D1InkStyle object, for use with ink rendering methods such as DrawInk.
old-location: direct2d\id2d1devicecontext2_createinkstyle.htm
tech.root: Direct2D
ms.assetid: 6d219a50-da5f-b5ff-e819-70b2dc5f538c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateInkStyle, CreateInkStyle method [Direct2D], CreateInkStyle method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateInkStyle method, ID2D1DeviceContext2.CreateInkStyle, ID2D1DeviceContext2.CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle), ID2D1DeviceContext2::CreateInkStyle, ID2D1DeviceContext2::CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle), d2d1_3/ID2D1DeviceContext2::CreateInkStyle, direct2d.id2d1devicecontext2_createinkstyle
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
 - ID2D1DeviceContext2.CreateInkStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext2::CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle)


## -description


Creates a new <a href="https://msdn.microsoft.com/03853FA5-1377-42FB-A4C2-50069DDF6E2D">ID2D1InkStyle</a> object, for use with ink 
        rendering methods such as <a href="https://msdn.microsoft.com/d7c27267-c0c3-d21c-7980-3d92396509c7">DrawInk</a>.


## -parameters




### -param inkStyleProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/81B9E108-D0A6-4F7E-8BE9-76A570B1D050">D2D1_INK_STYLE_PROPERTIES</a></b>

The properties of the ink style to be created.


### -param inkStyle [out]

Type: <b><a href="https://msdn.microsoft.com/03853FA5-1377-42FB-A4C2-50069DDF6E2D">ID2D1InkStyle</a>**</b>

When this method returns, contains the address of a pointer to a new ink style object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

