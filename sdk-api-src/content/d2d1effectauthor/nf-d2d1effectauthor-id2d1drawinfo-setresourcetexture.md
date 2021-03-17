---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetResourceTexture
title: ID2D1DrawInfo::SetResourceTexture (d2d1effectauthor.h)
description: Sets the resource texture corresponding to the given shader texture index.
helpviewer_keywords: ["ID2D1DrawInfo interface [Direct2D]","SetResourceTexture method","ID2D1DrawInfo.SetResourceTexture","ID2D1DrawInfo::SetResourceTexture","SetResourceTexture","SetResourceTexture method [Direct2D]","SetResourceTexture method [Direct2D]","ID2D1DrawInfo interface","d2d1effectauthor/ID2D1DrawInfo::SetResourceTexture","direct2d.id2d1drawinfo_setresourcetexture"]
old-location: direct2d\id2d1drawinfo_setresourcetexture.htm
tech.root: Direct2D
ms.assetid: 6E53577B-AD97-4530-8260-4A99B90E0581
ms.date: 12/05/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetResourceTexture method, ID2D1DrawInfo.SetResourceTexture, ID2D1DrawInfo::SetResourceTexture, SetResourceTexture, SetResourceTexture method [Direct2D], SetResourceTexture method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetResourceTexture, direct2d.id2d1drawinfo_setresourcetexture
req.header: d2d1effectauthor.h
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DrawInfo::SetResourceTexture
 - d2d1effectauthor/ID2D1DrawInfo::SetResourceTexture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1DrawInfo.SetResourceTexture
---

# ID2D1DrawInfo::SetResourceTexture


## -description

Sets the resource texture corresponding to the given shader texture index.

## -parameters

### -param textureIndex

Type: <b>UINT32</b>

The index of the texture to be bound to the pixel shader.

### -param resourceTexture [in]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1resourcetexture">ID2D1ResourceTexture</a>*</b>

The created resource texture.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo">ID2D1DrawInfo</a>