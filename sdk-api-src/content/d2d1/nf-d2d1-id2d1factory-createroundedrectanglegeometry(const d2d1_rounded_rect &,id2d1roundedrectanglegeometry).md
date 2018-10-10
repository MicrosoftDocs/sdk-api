---
UID: NF:d2d1.ID2D1Factory.CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry)
title: ID2D1Factory::CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry)
author: windows-sdk-content
description: Creates an ID2D1RoundedRectangleGeometry.
old-location: direct2d\ID2D1Factory_CreateRoundedRectangleGeometry_ref_D2D1_ROUNDED_RECT_ptr_ptr_ID2D1RoundedRectangleGeometry.htm
tech.root: Direct2D
ms.assetid: a779a6ad-2d86-416f-8f3f-1ccc90c13572
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CreateRoundedRectangleGeometry, CreateRoundedRectangleGeometry method [Direct2D], CreateRoundedRectangleGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateRoundedRectangleGeometry method, ID2D1Factory.CreateRoundedRectangleGeometry, ID2D1Factory.CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry), ID2D1Factory::CreateRoundedRectangleGeometry, ID2D1Factory::CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry), d2d1/ID2D1Factory::CreateRoundedRectangleGeometry, direct2d.ID2D1Factory_CreateRoundedRectangleGeometry_ref_D2D1_ROUNDED_RECT_ptr_ptr_ID2D1RoundedRectangleGeometry
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
 - ID2D1Factory.CreateRoundedRectangleGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry)


## -description


Creates an <a href="https://msdn.microsoft.com/e49e9be7-155a-4487-9931-035f18771c04">ID2D1RoundedRectangleGeometry</a>. 


## -parameters




### -param roundedRectangle [ref]

Type: <b>const <a href="https://msdn.microsoft.com/7069ca65-170e-42fc-8c1a-849a2f25c36f">D2D1_ROUNDED_RECT</a></b>

The coordinates and corner radii of the rounded rectangle geometry.


### -param roundedRectangleGeometry [out]

Type: <b><a href="https://msdn.microsoft.com/e49e9be7-155a-4487-9931-035f18771c04">ID2D1RoundedRectangleGeometry</a>**</b>

When this method returns, contains the address of the pointer to the rounded rectangle geometry created by this method.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

