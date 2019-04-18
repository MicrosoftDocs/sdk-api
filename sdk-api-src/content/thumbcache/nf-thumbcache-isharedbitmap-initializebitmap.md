---
UID: NF:thumbcache.ISharedBitmap.InitializeBitmap
title: ISharedBitmap::InitializeBitmap (thumbcache.h)
author: windows-sdk-content
description: Initializes a new ISharedBitmap object with a given bitmap.
old-location: shell\ISharedBitmap_InitializeBitmap.htm
tech.root: shell
ms.assetid: 55018484-df70-43fa-b494-215035b90ceb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISharedBitmap interface [Windows Shell],InitializeBitmap method, ISharedBitmap.InitializeBitmap, ISharedBitmap::InitializeBitmap, InitializeBitmap, InitializeBitmap method [Windows Shell], InitializeBitmap method [Windows Shell],ISharedBitmap interface, WTSAT_ARGB, WTSAT_RGB, WTSAT_UNKNOWN, _shell__InitializeBitmap, shell.ISharedBitmap_InitializeBitmap, thumbcache/ISharedBitmap::InitializeBitmap
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - ISharedBitmap.InitializeBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISharedBitmap::InitializeBitmap


## -description


Initializes a new <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object with a given bitmap.


## -parameters




### -param hbm [in]

Type: <b>HBITMAP</b>

A handle to the bitmap with which to initialize a new <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object. The bitmap must be a DIB.


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When an <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object is instantiated by the client (as opposed to being returned by the <a href="https://msdn.microsoft.com/3b5069e2-f20b-4c43-a9e7-334366980f5c">IThumbnailCache::GetThumbnailByID</a> or <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> methods), the underlying bitmap will not reside in shared memory.



