---
UID: NF:d2d1.ID2D1Factory.CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry)
title: ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry)
author: windows-sdk-content
description: Creates an ID2D1RectangleGeometry.
old-location: direct2d\ID2D1Factory_CreateRectangleGeometry_ptr_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry.htm
tech.root: direct2d
ms.assetid: 3d9a1e40-1432-4800-8d15-e2b8bda8f04f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateRectangleGeometry, CreateRectangleGeometry method [Direct2D], CreateRectangleGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateRectangleGeometry method, ID2D1Factory.CreateRectangleGeometry, ID2D1Factory.CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry), ID2D1Factory::CreateRectangleGeometry, ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry), d2d1/ID2D1Factory::CreateRectangleGeometry, direct2d.ID2D1Factory_CreateRectangleGeometry_ptr_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry
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
 - ID2D1Factory.CreateRectangleGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry)


## -description


Creates an <a href="https://msdn.microsoft.com/bb5f65ba-34d4-418b-863c-2431046bce8e">ID2D1RectangleGeometry</a>. 


## -parameters




### -param rectangle [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The coordinates of the rectangle geometry. 


### -param rectangleGeometry [out]

Type: <b><a href="https://msdn.microsoft.com/bb5f65ba-34d4-418b-863c-2431046bce8e">ID2D1RectangleGeometry</a>**</b>

When this method returns, contains the address of the pointer to the rectangle geometry created by this method.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

