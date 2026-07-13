---
UID: NF:thumbcache.ISharedBitmap.GetFormat
title: ISharedBitmap::GetFormat (thumbcache.h)
description: Retrieves the alpha type of the bitmap image.
helpviewer_keywords: ["GetFormat","GetFormat method [Windows Shell]","GetFormat method [Windows Shell]","ISharedBitmap interface","ISharedBitmap interface [Windows Shell]","GetFormat method","ISharedBitmap.GetFormat","ISharedBitmap::GetFormat","WTSAT_ARGB","WTSAT_RGB","_shell_ISharedBitmap_GetFormat","shell.ISharedBitmap_GetFormat","thumbcache/ISharedBitmap::GetFormat"]
old-location: shell\ISharedBitmap_GetFormat.htm
tech.root: shell
ms.assetid: 403b8b19-c96f-4205-999f-103025d2b923
ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [Windows Shell], GetFormat method [Windows Shell],ISharedBitmap interface, ISharedBitmap interface [Windows Shell],GetFormat method, ISharedBitmap.GetFormat, ISharedBitmap::GetFormat, WTSAT_ARGB, WTSAT_RGB, _shell_ISharedBitmap_GetFormat, shell.ISharedBitmap_GetFormat, thumbcache/ISharedBitmap::GetFormat
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
 - ISharedBitmap::GetFormat
 - thumbcache/ISharedBitmap::GetFormat
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
 - ISharedBitmap.GetFormat
---

# ISharedBitmap::GetFormat


## -description

Retrieves the alpha type of the bitmap image.

## -parameters

### -param pat [out]

Type: <b>WTS_ALPHATYPE*</b>

When this method returns, contains a pointer to the alpha type of the bitmap image. One of the following values.



#### WTSAT_RGB

The bitmap does not contain an alpha channel for transparency.



#### WTSAT_ARGB

The bitmap contains an alpha channel for transparency.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

