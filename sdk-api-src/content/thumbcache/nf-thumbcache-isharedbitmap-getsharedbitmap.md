---
UID: NF:thumbcache.ISharedBitmap.GetSharedBitmap
title: ISharedBitmap::GetSharedBitmap (thumbcache.h)
description: Retrieves the bitmap contained in an ISharedBitmap object.
helpviewer_keywords: ["GetSharedBitmap","GetSharedBitmap method [Windows Shell]","GetSharedBitmap method [Windows Shell]","ISharedBitmap interface","ISharedBitmap interface [Windows Shell]","GetSharedBitmap method","ISharedBitmap.GetSharedBitmap","ISharedBitmap::GetSharedBitmap","_shell__GetSharedBitmap","shell.ISharedBitmap_GetSharedBitmap","thumbcache/ISharedBitmap::GetSharedBitmap"]
old-location: shell\ISharedBitmap_GetSharedBitmap.htm
tech.root: shell
ms.assetid: 0d2cfdba-b51f-4035-b0b2-e48933505c73
ms.date: 12/05/2018
ms.keywords: GetSharedBitmap, GetSharedBitmap method [Windows Shell], GetSharedBitmap method [Windows Shell],ISharedBitmap interface, ISharedBitmap interface [Windows Shell],GetSharedBitmap method, ISharedBitmap.GetSharedBitmap, ISharedBitmap::GetSharedBitmap, _shell__GetSharedBitmap, shell.ISharedBitmap_GetSharedBitmap, thumbcache/ISharedBitmap::GetSharedBitmap
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISharedBitmap::GetSharedBitmap
 - thumbcache/ISharedBitmap::GetSharedBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - ISharedBitmap.GetSharedBitmap
---

# ISharedBitmap::GetSharedBitmap


## -description

Retrieves the bitmap contained in an <a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a> object.

## -parameters

### -param phbm [out]

Type: <b>HBITMAP*</b>

A pointer to a handle to the bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The bitmap retrieved might reside in shared memory.