---
UID: NF:d2d1.ID2D1Factory.CreateEllipseGeometry(const D2D1_ELLIPSE,ID2D1EllipseGeometry)
title: ID2D1Factory::CreateEllipseGeometry(const D2D1_ELLIPSE,ID2D1EllipseGeometry)
author: windows-sdk-content
description: Creates an ID2D1EllipseGeometry.
old-location: direct2d\ID2D1Factory_CreateEllipseGeometry_ptr_D2D1_ELLIPSE_ptr_ptr_ID2D1EllipseGeometry.htm
tech.root: direct2d
ms.assetid: 2c656119-b410-4269-85d0-5f0e5f430b7a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CreateEllipseGeometry, CreateEllipseGeometry method [Direct2D], CreateEllipseGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateEllipseGeometry method, ID2D1Factory.CreateEllipseGeometry, ID2D1Factory.CreateEllipseGeometry(const D2D1_ELLIPSE,ID2D1EllipseGeometry), ID2D1Factory::CreateEllipseGeometry, ID2D1Factory::CreateEllipseGeometry(const D2D1_ELLIPSE,ID2D1EllipseGeometry), d2d1/ID2D1Factory::CreateEllipseGeometry, direct2d.ID2D1Factory_CreateEllipseGeometry_ptr_D2D1_ELLIPSE_ptr_ptr_ID2D1EllipseGeometry
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
 - ID2D1Factory.CreateEllipseGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateEllipseGeometry(const D2D1_ELLIPSE,ID2D1EllipseGeometry)


## -description


Creates an <a href="https://msdn.microsoft.com/4ab6452c-6df8-46c0-9e0d-0cebc19d84ba">ID2D1EllipseGeometry</a>.


## -parameters




### -param ellipse [in]

Type: <b>const <a href="https://msdn.microsoft.com/6fed6c49-ba83-4c2b-af8a-04156ee317f0">D2D1_ELLIPSE</a>*</b>

A value that describes the center point, x-radius, and y-radius of the ellipse geometry.



### -param ellipseGeometry [out]

Type: <b><a href="https://msdn.microsoft.com/4ab6452c-6df8-46c0-9e0d-0cebc19d84ba">ID2D1EllipseGeometry</a>**</b>

When this method returns, contains the address of the pointer to the ellipse geometry created by this method.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

