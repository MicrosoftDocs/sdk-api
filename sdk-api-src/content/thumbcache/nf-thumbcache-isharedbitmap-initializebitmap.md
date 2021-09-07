---
UID: NF:thumbcache.ISharedBitmap.InitializeBitmap
title: ISharedBitmap::InitializeBitmap (thumbcache.h)
description: Initializes a new ISharedBitmap object with a given bitmap.
helpviewer_keywords: ["ISharedBitmap interface [Windows Shell]","InitializeBitmap method","ISharedBitmap.InitializeBitmap","ISharedBitmap::InitializeBitmap","InitializeBitmap","InitializeBitmap method [Windows Shell]","InitializeBitmap method [Windows Shell]","ISharedBitmap interface","WTSAT_ARGB","WTSAT_RGB","WTSAT_UNKNOWN","_shell__InitializeBitmap","shell.ISharedBitmap_InitializeBitmap","thumbcache/ISharedBitmap::InitializeBitmap"]
old-location: shell\ISharedBitmap_InitializeBitmap.htm
tech.root: shell
ms.assetid: 55018484-df70-43fa-b494-215035b90ceb
ms.date: 12/05/2018
ms.keywords: ISharedBitmap interface [Windows Shell],InitializeBitmap method, ISharedBitmap.InitializeBitmap, ISharedBitmap::InitializeBitmap, InitializeBitmap, InitializeBitmap method [Windows Shell], InitializeBitmap method [Windows Shell],ISharedBitmap interface, WTSAT_ARGB, WTSAT_RGB, WTSAT_UNKNOWN, _shell__InitializeBitmap, shell.ISharedBitmap_InitializeBitmap, thumbcache/ISharedBitmap::InitializeBitmap
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
 - ISharedBitmap::InitializeBitmap
 - thumbcache/ISharedBitmap::InitializeBitmap
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
 - ISharedBitmap.InitializeBitmap
---

# ISharedBitmap::InitializeBitmap


## -description

Initializes a new <a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a> object with a given bitmap.

## -parameters

### -param hbm [in]

Type: <b>HBITMAP</b>

A handle to the bitmap with which to initialize a new <a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a> object. The bitmap must be a DIB.

### -param wtsAT [in]

Type: <b>WTS_ALPHATYPE</b>

The alpha type of the bitmap image.  May be one of the following values.



#### WTSAT_UNKNOWN

Cannot determine whether the bitmap has an alpha channel.



#### WTSAT_RGB

The bitmap does not contain an alpha channel for transparency.



#### WTSAT_ARGB

The bitmap contains an alpha channel for transparency.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When an <a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a> object is instantiated by the client (as opposed to being returned by the <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnailbyid">IThumbnailCache::GetThumbnailByID</a> or <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a> methods), the underlying bitmap will not reside in shared memory.