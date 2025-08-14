---
UID: NF:vfw.ICSetState
title: ICSetState macro (vfw.h)
description: The ICSetState macro notifies a video compression driver to set the state of the compressor. You can use this macro or explicitly call the ICM_SETSTATE message.
helpviewer_keywords: ["ICSetState","ICSetState macro [Windows Multimedia]","_win32_ICSetState","multimedia.icsetstate","vfw/ICSetState"]
old-location: multimedia\icsetstate.htm
tech.root: Multimedia
ms.assetid: 96958fbf-8539-49bc-a2ff-160b7ea8d2ab
ms.date: 07/01/2025
ms.keywords: ICSetState, ICSetState macro [Windows Multimedia], _win32_ICSetState, multimedia.icsetstate, vfw/ICSetState
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ICSetState
 - vfw/ICSetState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICSetState
---

# ICSetState macro

## -syntax

```cpp
DWORD ICSetState(
     hic,
     pv,
     cb
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the number of bytes used by the compressor if successful or zero otherwise.


## -description

The <b>ICSetState</b> macro notifies a video compression driver to set the state of the compressor. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-setstate">ICM_SETSTATE</a> message.

## -parameters

### -param hic

Handle of the compressor.

### -param pv

Pointer to a block of memory containing configuration data. You can specify <b>NULL</b> for this parameter to reset the compressor to its default state.

### -param cb

Size, in bytes, of the block of memory.

## -remarks

The information used by this message is private and specific to a given compressor. Client applications should use this message only to restore information previously obtained with the <a href="/windows/desktop/api/vfw/nf-vfw-icgetstate">ICGetState</a> and <a href="/windows/desktop/api/vfw/nf-vfw-icconfigure">ICConfigure</a> macros and should use the <b>ICConfigure</b> macro to adjust the configuration of a video compression driver.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
