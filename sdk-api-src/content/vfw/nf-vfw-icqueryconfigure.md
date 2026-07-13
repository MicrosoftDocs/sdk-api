---
UID: NF:vfw.ICQueryConfigure
title: ICQueryConfigure macro (vfw.h)
description: The ICQueryConfigure macro queries a video compression driver to determine if it has a configuration dialog box. You can use this macro or explicitly send the ICM_CONFIGURE message.
helpviewer_keywords: ["ICQueryConfigure","ICQueryConfigure macro [Windows Multimedia]","_win32_ICQueryConfigure","multimedia.icqueryconfigure","vfw/ICQueryConfigure"]
old-location: multimedia\icqueryconfigure.htm
tech.root: Multimedia
ms.assetid: a0e65123-5224-43a4-9a1e-28a10ecbed5c
ms.date: 07/01/2025
ms.keywords: ICQueryConfigure, ICQueryConfigure macro [Windows Multimedia], _win32_ICQueryConfigure, multimedia.icqueryconfigure, vfw/ICQueryConfigure
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
 - ICQueryConfigure
 - vfw/ICQueryConfigure
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
 - ICQueryConfigure
---

# ICQueryConfigure macro

## -syntax

```cpp
DWORD ICQueryConfigure(
     hic
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the driver supports this macro or ICERR_UNSUPPORTED otherwise.


## -description

The <b>ICQueryConfigure</b> macro queries a video compression driver to determine if it has a configuration dialog box. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/icm-configure">ICM_CONFIGURE</a> message.

## -parameters

### -param hic

Handle of the compressor.

## -remarks

This message is different from the <a href="/windows/desktop/Multimedia/drv-configure">DRV_CONFIGURE</a> message used for hardware configuration. The dialog box for this message should let the user set and edit the internal state referenced by the <a href="/windows/desktop/Multimedia/icm-getstate">ICM_GETSTATE</a> and <a href="/windows/desktop/Multimedia/icm-setstate">ICM_SETSTATE</a> messages. For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
