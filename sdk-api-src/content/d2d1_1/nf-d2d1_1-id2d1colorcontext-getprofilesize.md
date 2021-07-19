---
UID: NF:d2d1_1.ID2D1ColorContext.GetProfileSize
title: ID2D1ColorContext::GetProfileSize (d2d1_1.h)
description: Gets the size of the color profile associated with the bitmap.
helpviewer_keywords: ["GetProfileSize","GetProfileSize method [Direct2D]","GetProfileSize method [Direct2D]","ID2D1ColorContext interface","ID2D1ColorContext interface [Direct2D]","GetProfileSize method","ID2D1ColorContext.GetProfileSize","ID2D1ColorContext::GetProfileSize","d2d1_1/ID2D1ColorContext::GetProfileSize","direct2d.id2d1colorcontext_getprofilesize"]
old-location: direct2d\id2d1colorcontext_getprofilesize.htm
tech.root: Direct2D
ms.assetid: ceae8c7d-80b5-4052-ac43-85f9802c209e
ms.date: 12/05/2018
ms.keywords: GetProfileSize, GetProfileSize method [Direct2D], GetProfileSize method [Direct2D],ID2D1ColorContext interface, ID2D1ColorContext interface [Direct2D],GetProfileSize method, ID2D1ColorContext.GetProfileSize, ID2D1ColorContext::GetProfileSize, d2d1_1/ID2D1ColorContext::GetProfileSize, direct2d.id2d1colorcontext_getprofilesize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ColorContext::GetProfileSize
 - d2d1_1/ID2D1ColorContext::GetProfileSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1ColorContext.GetProfileSize
---

# ID2D1ColorContext::GetProfileSize


## -description

Gets the size of the color profile associated with the bitmap.



## -returns

Type: <b>UINT32</b>

This method returns the  size of the profile in bytes.

## -remarks

This can be used to allocate a buffer to receive the color profile bytes associated with the context.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getcolorcontext">ID2D1Bitmap1::GetColorContext</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1colorcontext-getprofile">ID2D1ColorContext::GetProfile</a>
