---
UID: NF:d2d1_1.ID2D1Bitmap1.GetColorContext
title: ID2D1Bitmap1::GetColorContext (d2d1_1.h)
description: Gets the color context information associated with the bitmap.
helpviewer_keywords: ["GetColorContext","GetColorContext method [Direct2D]","GetColorContext method [Direct2D]","ID2D1Bitmap1 interface","ID2D1Bitmap1 interface [Direct2D]","GetColorContext method","ID2D1Bitmap1.GetColorContext","ID2D1Bitmap1::GetColorContext","d2d1_1/ID2D1Bitmap1::GetColorContext","direct2d.id2d1bitmap1_getcolorcontext"]
old-location: direct2d\id2d1bitmap1_getcolorcontext.htm
tech.root: Direct2D
ms.assetid: 7ab8bed5-c124-4e14-8a05-3a71f07f5fd1
ms.date: 12/05/2018
ms.keywords: GetColorContext, GetColorContext method [Direct2D], GetColorContext method [Direct2D],ID2D1Bitmap1 interface, ID2D1Bitmap1 interface [Direct2D],GetColorContext method, ID2D1Bitmap1.GetColorContext, ID2D1Bitmap1::GetColorContext, d2d1_1/ID2D1Bitmap1::GetColorContext, direct2d.id2d1bitmap1_getcolorcontext
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
 - ID2D1Bitmap1::GetColorContext
 - d2d1_1/ID2D1Bitmap1::GetColorContext
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
 - ID2D1Bitmap1.GetColorContext
---

# ID2D1Bitmap1::GetColorContext


## -description

Gets the color context information associated with the bitmap.

## -parameters

### -param colorContext [out, optional]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>**</b>

When this method returns, contains the address of a pointer to the  color context interface associated with the bitmap.

## -remarks

If the bitmap was created without specifying a color context, the returned context is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>