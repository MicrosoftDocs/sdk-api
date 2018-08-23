---
UID: NF:d2d1_1.ID2D1Bitmap1.GetColorContext
title: ID2D1Bitmap1::GetColorContext
author: windows-sdk-content
description: Gets the color context information associated with the bitmap.
old-location: direct2d\id2d1bitmap1_getcolorcontext.htm
old-project: direct2d
ms.assetid: 7ab8bed5-c124-4e14-8a05-3a71f07f5fd1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetColorContext, GetColorContext method [Direct2D], GetColorContext method [Direct2D],ID2D1Bitmap1 interface, ID2D1Bitmap1 interface [Direct2D],GetColorContext method, ID2D1Bitmap1.GetColorContext, ID2D1Bitmap1::GetColorContext, d2d1_1/ID2D1Bitmap1::GetColorContext, direct2d.id2d1bitmap1_getcolorcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_UNIT_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Bitmap1.GetColorContext
product: Windows
targetos: Windows
req.lib: 
req.dll: D2d1.dll
req.irql: 
---

# ID2D1Bitmap1::GetColorContext


## -description


Gets the color context information associated with the bitmap.


## -parameters




### -param colorContext [out, optional]

Type: <b><a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>**</b>

When this method returns, contains the address of a pointer to the  color context interface associated with the bitmap.


## -returns



This method does not return a value.




## -remarks



If the bitmap was created without specifying a color context, the returned context is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>
 

 

