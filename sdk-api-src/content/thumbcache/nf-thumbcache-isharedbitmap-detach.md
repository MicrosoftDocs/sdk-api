---
UID: NF:thumbcache.ISharedBitmap.Detach
title: ISharedBitmap::Detach (thumbcache.h)
description: Retrieves the bitmap contained in an ISharedBitmap object, and returns a copy if the contained bitmap resides in shared memory.
helpviewer_keywords: ["Detach","Detach method [Windows Shell]","Detach method [Windows Shell]","ISharedBitmap interface","ISharedBitmap interface [Windows Shell]","Detach method","ISharedBitmap.Detach","ISharedBitmap::Detach","_shell__Detach","shell.ISharedBitmap_Detach","thumbcache/ISharedBitmap::Detach"]
old-location: shell\ISharedBitmap_Detach.htm
tech.root: shell
ms.assetid: 1d68beca-c254-435e-a1cd-04e7aa462c84
ms.date: 12/05/2018
ms.keywords: Detach, Detach method [Windows Shell], Detach method [Windows Shell],ISharedBitmap interface, ISharedBitmap interface [Windows Shell],Detach method, ISharedBitmap.Detach, ISharedBitmap::Detach, _shell__Detach, shell.ISharedBitmap_Detach, thumbcache/ISharedBitmap::Detach
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
 - ISharedBitmap::Detach
 - thumbcache/ISharedBitmap::Detach
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
 - ISharedBitmap.Detach
---

# ISharedBitmap::Detach


## -description

Retrieves the bitmap contained in an <a href="/windows/desktop/api/thumbcache/nn-thumbcache-isharedbitmap">ISharedBitmap</a> object, and returns a copy if the contained bitmap resides in shared memory. After calling this method the bitmap is no longer associated with this <b>ISharedBitmap</b> and you cannot call <a href="/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-getsharedbitmap">ISharedBitmap::GetSharedBitmap</a> or <b>ISharedBitmap::Detach</b> on it again.

## -parameters

### -param phbm [out]

Type: <b>HBITMAP*</b>

When this method returns, contains a pointer to a handle to the bitmap to retrieve.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the bitmap being retrieved resides in shared memory, a copy of the bitmap is returned.  The <b>Detach</b> method does not release any references to the underlying shared memory.

If the bitmap being retrieved does not reside in shared memory, the bitmap itself is returned and no copy is made.