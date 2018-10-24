---
UID: NF:d2d1_1.ID2D1ColorContext.GetProfileSize
title: ID2D1ColorContext::GetProfileSize
author: windows-sdk-content
description: Gets the size of the color profile associated with the bitmap.
old-location: direct2d\id2d1colorcontext_getprofilesize.htm
tech.root: Direct2D
ms.assetid: ceae8c7d-80b5-4052-ac43-85f9802c209e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetProfileSize, GetProfileSize method [Direct2D], GetProfileSize method [Direct2D],ID2D1ColorContext interface, ID2D1ColorContext interface [Direct2D],GetProfileSize method, ID2D1ColorContext.GetProfileSize, ID2D1ColorContext::GetProfileSize, d2d1_1/ID2D1ColorContext::GetProfileSize, direct2d.id2d1colorcontext_getprofilesize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
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
 - ID2D1ColorContext.GetProfileSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ColorContext::GetProfileSize


## -description


Gets the size of the color profile associated with the bitmap. 	


## -parameters






## -returns



Type: <b>UINT32</b>

This method returns the  size of the profile in bytes.




## -remarks



This can be used to allocate a buffer to receive the color profile bytes associated with the context.




## -see-also




<a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a>



<a href="https://msdn.microsoft.com/7ab8bed5-c124-4e14-8a05-3a71f07f5fd1">ID2D1Bitmap1::GetColorContext</a>



<a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>



<a href="https://msdn.microsoft.com/f6beae12-e02d-432b-b9d8-5e1206e3c482">ID2D1ColorContext::GetProfile</a>
 

 

