---
UID: NE:d2d1_1.D2D1_THREADING_MODE
title: D2D1_THREADING_MODE (d2d1_1.h)
description: Specifies the threading mode used while simultaneously creating the device, factory, and device context.
helpviewer_keywords: ["D2D1_THREADING_MODE","D2D1_THREADING_MODE enumeration [Direct2D]","D2D1_THREADING_MODE_MULTI_THREADED","D2D1_THREADING_MODE_SINGLE_THREADED","d2d1_1/D2D1_THREADING_MODE","d2d1_1/D2D1_THREADING_MODE_MULTI_THREADED","d2d1_1/D2D1_THREADING_MODE_SINGLE_THREADED","direct2d.__d2d1_threading_mode"]
old-location: direct2d\__d2d1_threading_mode.htm
tech.root: Direct2D
ms.assetid: 21fba5ee-3d31-4142-b66a-94b343e1c6eb
ms.date: 12/05/2018
ms.keywords: D2D1_THREADING_MODE, D2D1_THREADING_MODE enumeration [Direct2D], D2D1_THREADING_MODE_MULTI_THREADED, D2D1_THREADING_MODE_SINGLE_THREADED, d2d1_1/D2D1_THREADING_MODE, d2d1_1/D2D1_THREADING_MODE_MULTI_THREADED, d2d1_1/D2D1_THREADING_MODE_SINGLE_THREADED, direct2d.__d2d1_threading_mode
req.header: d2d1_1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_THREADING_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_THREADING_MODE
 - d2d1_1/D2D1_THREADING_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_1.h
api_name:
 - D2D1_THREADING_MODE
---

# D2D1_THREADING_MODE enumeration


## -description

Specifies the threading mode used while simultaneously creating the device, factory, and device context.

## -enum-fields

### -field D2D1_THREADING_MODE_SINGLE_THREADED

Resources may only be invoked serially.  Device context state is not protected from multi-threaded access.

### -field D2D1_THREADING_MODE_MULTI_THREADED

Resources may be invoked from multiple threads. Resources use interlocked reference counting and their state is protected.

### -field D2D1_THREADING_MODE_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_creation_properties">D2D1_CREATION_PROPERTIES</a>



<a href="/windows/desktop/Direct2D/multi-threaded-direct2d-apps">Multithreaded Direct2D Apps</a>
