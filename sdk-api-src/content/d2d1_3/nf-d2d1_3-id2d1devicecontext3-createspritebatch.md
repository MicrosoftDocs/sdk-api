---
UID: NF:d2d1_3.ID2D1DeviceContext3.CreateSpriteBatch
title: ID2D1DeviceContext3::CreateSpriteBatch (d2d1_3.h)
author: windows-sdk-content
description: Creates a new, empty sprite batch. After creating a sprite batch, use ID2D1SpriteBatch::AddSprites to add sprites to it, then use ID2D1DeviceContext3::DrawSpriteBatch to draw it.
old-location: direct2d\id2d1devicecontext3_createspritebatch.htm
tech.root: Direct2D
ms.assetid: C9CCDF6B-BAEC-4C37-B3C1-60D50BACF973
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateSpriteBatch, CreateSpriteBatch method [Direct2D], CreateSpriteBatch method [Direct2D],ID2D1DeviceContext3 interface, ID2D1DeviceContext3 interface [Direct2D],CreateSpriteBatch method, ID2D1DeviceContext3.CreateSpriteBatch, ID2D1DeviceContext3::CreateSpriteBatch, d2d1_3/ID2D1DeviceContext3::CreateSpriteBatch, direct2d.id2d1devicecontext3_createspritebatch
ms.topic: method
f1_keywords: 
 - "d2d1_3/ID2D1DeviceContext3.CreateSpriteBatch"
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ID2D1DeviceContext3.CreateSpriteBatch
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext3::CreateSpriteBatch


## -description


Creates a new, empty sprite batch. After creating a sprite batch, use <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1spritebatch-addsprites">ID2D1SpriteBatch::AddSprites</a> 
        to add sprites to it, then use <a href="https://docs.microsoft.com/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)">ID2D1DeviceContext3::DrawSpriteBatch</a> to draw it.


## -parameters




### -param spriteBatch [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1spritebatch">ID2D1SpriteBatch</a>**</b>

When this method returns, contains a pointer to a new, empty sprite batch to be populated by the app.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext3">ID2D1DeviceContext3</a>
 

 

