---
UID: NF:xapo.XAPOAlloc
title: XAPOAlloc macro (xapo.h)
description: Memory allocation macro used by IXAPO methods that must allocate arbitrary sized structures that are subsequently returned to the application.
helpviewer_keywords: ["XAPOAlloc","XAPOAlloc macro [XAudio2 Audio Mixing APIs]","xapo/XAPOAlloc","xaudio2.xapoalloc"]
old-location: xaudio2\xapoalloc.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xapo.XAPOAlloc(ULONG)
ms.date: 07/01/2025
ms.keywords: XAPOAlloc, XAPOAlloc macro [XAudio2 Audio Mixing APIs], xapo/XAPOAlloc, xaudio2.xapoalloc
req.header: xapo.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAPOAlloc
 - xapo/XAPOAlloc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XAPO.h
api_name:
 - XAPOAlloc
---

# XAPOAlloc macro

## -syntax

```cpp
LPVOID XAPOAlloc(
    ULONG size
);
```

## -returns

Type: **LPVOID**

Allocated memory block; returns **NULL** if insufficient memory available.


## -description

Memory allocation macro used by IXAPO methods that must allocate arbitrary sized structures that are subsequently returned to the application.

## -parameters

### -param size

Size, in bytes, of the memory block to be allocated.

## -remarks

<a href="/windows/desktop/api/xapo/nf-xapo-xapofree">XAPOFree</a> and <b>XAPOAlloc</b> are memory allocation macros that allow one module to allocate memory and another to free it, by guaranteeing that the same heap manager is used regardless of differences between the build environments of the two modules.

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/xapo/nf-xapo-xapofree">XAPOFree</a> and <b>XAPOAlloc</b> resolve to <b>XMemAlloc</b> and <b>XMemFree</b> on Xbox 360.</td>
</tr>
</table>
 

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/xapo/nf-xapo-xapofree">XAPOFree</a> and <b>XAPOAlloc</b> resolve to <b>CoTaskMemAlloc</b> and <b>CoTaskMemFree</b>.</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/macros">Macros</a>
