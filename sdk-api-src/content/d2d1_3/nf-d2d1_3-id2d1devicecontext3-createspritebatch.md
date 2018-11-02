---
UID: NF:d2d1_3.ID2D1DeviceContext3.CreateSpriteBatch
title: ID2D1DeviceContext3::CreateSpriteBatch
author: windows-sdk-content
description: Creates a new, empty sprite batch. After creating a sprite batch, use ID2D1SpriteBatch::AddSprites to add sprites to it, then use ID2D1DeviceContext3::DrawSpriteBatch to draw it.
old-location: direct2d\id2d1devicecontext3_createspritebatch.htm
tech.root: direct2d
ms.assetid: C9CCDF6B-BAEC-4C37-B3C1-60D50BACF973
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateSpriteBatch, CreateSpriteBatch method [Direct2D], CreateSpriteBatch method [Direct2D],ID2D1DeviceContext3 interface, ID2D1DeviceContext3 interface [Direct2D],CreateSpriteBatch method, ID2D1DeviceContext3.CreateSpriteBatch, ID2D1DeviceContext3::CreateSpriteBatch, d2d1_3/ID2D1DeviceContext3::CreateSpriteBatch, direct2d.id2d1devicecontext3_createspritebatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext3::CreateSpriteBatch


## -description


Creates a new, empty sprite batch. After creating a sprite batch, use <a href="https://msdn.microsoft.com/49EA1F42-76C3-4505-B46A-422A336A13F6">ID2D1SpriteBatch::AddSprites</a> 
        to add sprites to it, then use <a href="https://msdn.microsoft.com/66d049ca-5d4b-1570-3fa3-8991f9fc97a0">ID2D1DeviceContext3::DrawSpriteBatch</a> to draw it.


## -parameters




### -param spriteBatch [out]

Type: <b><a href="https://msdn.microsoft.com/D33958D5-D31C-47DC-B172-CADB1F1B81AE">ID2D1SpriteBatch</a>**</b>

When this method returns, contains a pointer to a new, empty sprite batch to be populated by the app.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/AD763619-7880-41EB-8446-2E4B84CB4EAC">ID2D1DeviceContext3</a>
 

 

