---
UID: NF:d2d1.ID2D1TransformedGeometry.GetTransform
title: ID2D1TransformedGeometry::GetTransform
author: windows-sdk-content
description: Retrieves the matrix used to transform the ID2D1TransformedGeometry object's source geometry.
old-location: direct2d\ID2D1TransformedGeometry_GetTransform.htm
tech.root: Direct2D
ms.assetid: 9d448af2-49ad-4209-b3a6-b07b40bb3e9d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetTransform, GetTransform method [Direct2D], GetTransform method [Direct2D],ID2D1TransformedGeometry interface, ID2D1TransformedGeometry interface [Direct2D],GetTransform method, ID2D1TransformedGeometry.GetTransform, ID2D1TransformedGeometry::GetTransform, d2d1/ID2D1TransformedGeometry::GetTransform, direct2d.ID2D1TransformedGeometry_GetTransform
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
 - ID2D1TransformedGeometry.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TransformedGeometry::GetTransform


## -description


Retrieves the matrix used to transform the <a href="https://msdn.microsoft.com/5d48eab6-1229-4e54-bfab-602b471b23a4">ID2D1TransformedGeometry</a> object's source geometry.


## -parameters




### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

A pointer that receives the matrix used to transform the <a href="https://msdn.microsoft.com/5d48eab6-1229-4e54-bfab-602b471b23a4">ID2D1TransformedGeometry</a> object's source geometry. You must allocate storage for this parameter.  


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/5d48eab6-1229-4e54-bfab-602b471b23a4">ID2D1TransformedGeometry</a>
 

 

