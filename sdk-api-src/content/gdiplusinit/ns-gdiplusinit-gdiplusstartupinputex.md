---
UID: NS:gdiplusinit.GdiplusStartupInputEx
title: GdiplusStartupInputEx
ms.date: 01/15/2025
targetos: Windows
description: The **GdiplusStartupInputEx** structure holds a block of arguments that are required by the [GdiplusStartup](../gdiplusinit/nf-gdiplusinit-gdiplusstartup.md) function.
tech.root: gdiplus
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: gdiplusinit.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - gdiplusinit.h
api_name:
 - GdiplusStartupInputEx
f1_keywords:
 - GdiplusStartupInputEx
 - gdiplusinit/GdiplusStartupInputEx
dev_langs:
 - c++
prerelease: true
---

## -description

The **GdiplusStartupInputEx** structure holds a block of arguments that are required by the [GdiplusStartup](/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup) function. **GdiplusStartupInputEx** derives from [**GdiplusStartupInput**](/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartupinput-gdiplusstartupinput).

## -struct-fields

### -field StartupParameters

Type: **INT**

See [**GdiplusStartupParams**](./ne-gdiplusinit-gdiplusstartupparams.md). The default value is **GdiplusStartupDefault** (0).

## -remarks

> ![IMPORTANT]
> For info about operating system (OS) support for the codecs mentioned below, see [Media Feature Pack for Windows 10/11 N (September 2022)](https://support.microsoft.com/windows/media-feature-pack-for-windows-10-11-n-september-2022-78cfeea5-c7d9-4aa8-b38f-ee4df1392009).

The **GdiplusStartupInputEx** structure also defines the following enumeration, which is the type of one of the parameters of the [GdiplusStartupInputEx.GdiplusStartupInputEx(Version,INT,DebugEventProc,BOOL,BOOL)](./nf-gdiplusinit-gdiplusstartupinputex-gdiplusstartupinputex(version_int_debugeventproc_bool_bool).md) constructor.

```cpp
enum class Version : UINT32
{
  V2 = 2,
  V3 = 3 // Enables Heif and Avif image codecs.
         // Unlike other functionalities in Gdiplus,
         // these two codecs require COM to be initialized.
};
```

## -see-also
