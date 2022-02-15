---
UID: NF:d2d1.ID2D1Factory.CreatePathGeometry
title: ID2D1Factory::CreatePathGeometry (d2d1.h)
description: Creates an empty ID2D1PathGeometry.
helpviewer_keywords: ["CreatePathGeometry","CreatePathGeometry method [Direct2D]","CreatePathGeometry method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreatePathGeometry method","ID2D1Factory.CreatePathGeometry","ID2D1Factory::CreatePathGeometry","d2d1/ID2D1Factory::CreatePathGeometry","direct2d.ID2D1Factory_CreatePathGeometry"]
old-location: direct2d\ID2D1Factory_CreatePathGeometry.htm
tech.root: Direct2D
ms.assetid: 35c46055-3df2-44d5-b11d-520ab2fa4a0e
ms.date: 12/05/2018
ms.keywords: CreatePathGeometry, CreatePathGeometry method [Direct2D], CreatePathGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreatePathGeometry method, ID2D1Factory.CreatePathGeometry, ID2D1Factory::CreatePathGeometry, d2d1/ID2D1Factory::CreatePathGeometry, direct2d.ID2D1Factory_CreatePathGeometry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory::CreatePathGeometry
 - d2d1/ID2D1Factory::CreatePathGeometry
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
 - ID2D1Factory.CreatePathGeometry
---

# ID2D1Factory::CreatePathGeometry


## -description

Creates an empty <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>.

## -parameters

### -param pathGeometry [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>**</b>

When this method returns, contains the address to a pointer to the path geometry created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

