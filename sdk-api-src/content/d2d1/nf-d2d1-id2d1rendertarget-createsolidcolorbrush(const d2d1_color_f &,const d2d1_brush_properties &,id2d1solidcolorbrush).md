---
UID: NF:d2d1.ID2D1RenderTarget.CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush)
title: ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush)
author: windows-sdk-content
description: Creates a new ID2D1SolidColorBrush that has the specified color and opacity.
old-location: direct2d\ID2D1RenderTarget_CreateSolidColorBrush_ref_COLOR_F_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1SolidColorBrush.htm
tech.root: direct2d
ms.assetid: c6597602-92b2-491c-b9f3-5a44a6980b80
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CreateSolidColorBrush, CreateSolidColorBrush method [Direct2D], CreateSolidColorBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateSolidColorBrush method, ID2D1RenderTarget.CreateSolidColorBrush, ID2D1RenderTarget.CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush), ID2D1RenderTarget::CreateSolidColorBrush, ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush), d2d1/ID2D1RenderTarget::CreateSolidColorBrush, direct2d.ID2D1RenderTarget_CreateSolidColorBrush_ref_COLOR_F_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1SolidColorBrush
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
 - ID2D1RenderTarget.CreateSolidColorBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateSolidColorBrush(const D2D1_COLOR_F &,const D2D1_BRUSH_PROPERTIES &,ID2D1SolidColorBrush)


## -description


Creates a new <a href="https://msdn.microsoft.com/a15c2696-3122-461e-806e-2195a50a3e92">ID2D1SolidColorBrush</a> that has the specified color and opacity.


## -parameters




### -param color [ref]

Type: <b>const <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The red, green, blue, and alpha values of the brush's color.


### -param brushProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a></b>

The base opacity of the brush.


### -param solidColorBrush [out]

Type: <b><a href="https://msdn.microsoft.com/a15c2696-3122-461e-806e-2195a50a3e92">ID2D1SolidColorBrush</a>**</b>

When this method returns, contains the address of a pointer to the new brush. This parameter is passed uninitialized.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/19d9ad76-b1e3-449f-8582-e00287b05874">Direct2D QuickStart</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

