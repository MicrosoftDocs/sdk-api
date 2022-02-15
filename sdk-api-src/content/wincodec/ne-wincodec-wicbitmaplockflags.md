---
UID: NE:wincodec.WICBitmapLockFlags
title: WICBitmapLockFlags (wincodec.h)
description: Specifies access to an IWICBitmap.
helpviewer_keywords: ["WICBitmapLockFlags","WICBitmapLockFlags enumeration [Windows Imaging Component]","WICBitmapLockRead","WICBitmapLockWrite","_wic_codec_wicbitmaplockflags","wic._wic_codec_wicbitmaplockflags","wincodec/WICBitmapLockFlags","wincodec/WICBitmapLockRead","wincodec/WICBitmapLockWrite"]
old-location: wic\_wic_codec_wicbitmaplockflags.htm
tech.root: wic
ms.assetid: d4d1bb38-3d1a-4e1e-a889-0491f3c01822
ms.date: 12/05/2018
ms.keywords: WICBitmapLockFlags, WICBitmapLockFlags enumeration [Windows Imaging Component], WICBitmapLockRead, WICBitmapLockWrite, _wic_codec_wicbitmaplockflags, wic._wic_codec_wicbitmaplockflags, wincodec/WICBitmapLockFlags, wincodec/WICBitmapLockRead, wincodec/WICBitmapLockWrite
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICBitmapLockFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICBitmapLockFlags
 - wincodec/WICBitmapLockFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICBitmapLockFlags
---

# WICBitmapLockFlags enumeration


## -description

Specifies access to an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>.

## -enum-fields

### -field WICBitmapLockRead:0x1

A read access lock.

### -field WICBitmapLockWrite:0x2

A write access lock.

### -field WICBITMAPLOCKFLAGS_FORCE_DWORD:0x7fffffff
