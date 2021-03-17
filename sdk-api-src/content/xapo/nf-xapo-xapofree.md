---
UID: NF:xapo.XAPOFree
title: XAPOFree macro (xapo.h)
description: Macro used to free memory allocated with the XAPOAlloc macro.
helpviewer_keywords: ["XAPOFree","XAPOFree macro [XAudio2 Audio Mixing APIs]","xapo/XAPOFree","xaudio2.xapofree"]
old-location: xaudio2\xapofree.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xapo.XAPOFree(void)
ms.date: 12/05/2018
ms.keywords: XAPOFree, XAPOFree macro [XAudio2 Audio Mixing APIs], xapo/XAPOFree, xaudio2.xapofree
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
 - XAPOFree
 - xapo/XAPOFree
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
 - XAPOFree
---

# XAPOFree macro


## -description

Macro used to free memory allocated with the <a href="/windows/desktop/api/xapo/nf-xapo-xapoalloc">XAPOAlloc</a> macro.

## -parameters

### -param p

Pointer to the memory block to be freed.

## -remarks

<b>XAPOFree</b> and <a href="/windows/desktop/api/xapo/nf-xapo-xapoalloc">XAPOAlloc</a> are memory allocation macros that allow one module to allocate memory and another to free it, by guaranteeing that the same heap manager is used regardless of differences between the build environments of the two modules.

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td><b>XAPOFree</b> and <a href="/windows/desktop/api/xapo/nf-xapo-xapoalloc">XAPOAlloc</a> resolve to <b>XMemAlloc</b> and <b>XMemFree</b> on Xbox 360.</td>
</tr>
</table>
 

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td><b>XAPOFree</b> and <a href="/windows/desktop/api/xapo/nf-xapo-xapoalloc">XAPOAlloc</a> resolve to <b>CoTaskMemAlloc</b> and <b>CoTaskMemFree</b>.</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/macros">Macros</a>