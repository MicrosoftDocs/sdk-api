---
UID: NF:gdiplusinit.GdiplusStartupInputEx.GdiplusStartupInputEx(Version,INT,DebugEventProc,BOOL,BOOL)
title: GdiplusStartupInputEx::GdiplusStartupInputEx(Version,INT,DebugEventProc,BOOL,BOOL)
description: Constructor for the GdiplusStartupInputEx structure.
tech.root: gdiplus
ms.date: 02/26/2024
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusinit.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - gdiplusinit.h
api_name:
 - GdiplusStartupInputEx::GdiplusStartupInputEx
f1_keywords:
 - GdiplusStartupInputEx::GdiplusStartupInputEx
 - gdiplusinit/GdiplusStartupInputEx::GdiplusStartupInputEx
dev_langs:
 - c++
helpviewer_keywords:
 - GdiplusStartupInputEx
prerelease: true
---

## -description

Constructor for the [**GdiplusStartupInputEx**](./ns-gdiplusinit-gdiplusstartupinputex.md) structure.

All of the constructor parameters are optional, so you can declare a variable of type **GdiplusStartupInputEx** without passing any arguments to the constructor, and all of the members will be initialized with appropriate default values.

## -parameters

### -param gdiplusVersion

Type: **Version**

The version of GDI+ to initialize. See the definition of the **Version** enum below.

```cpp
enum class Version : UINT32
{
  V2 = 2,
  V3 = 3 // Enables Heif and Avif image codecs.
         // Unlike other functionalities in Gdiplus,
         // these two codecs require COM to be initialized.
};
```

### -param startupParameters

Type: **INT**

See [**GdiplusStartupParams**](./ne-gdiplusinit-gdiplusstartupparams.md). The default value is **GdiplusStartupDefault** (0).

### -param debugEventCallback

Type: **[DebugEventProc](./nc-gdiplusinit-debugeventproc.md)**

Pointer to your [**DebugEventProc**](./nc-gdiplusinit-debugeventproc.md) callback function, which GDI+ can call on debug builds for assertions and warnings. The default value is **NULL**.

### -param suppressBackgroundThread

Type: **BOOL**

Boolean value that specifies whether to suppress the GDI+ background thread. If you pass **TRUE**, then [**GdiplusStartup**](./nf-gdiplusinit-gdiplusstartup.md) returns (in its *output* parameter) a pointer to a hook function, and a pointer to an unhook function. You must call those functions appropriately to replace the background thread. If you don't want to be responsible for calling the hook and unhook functions, then set this member to **FALSE**. The default value is **FALSE**.

### -param suppressExternalCodecs

Type: **BOOL**

Boolean value that specifies whether you want GDI+ to suppress external image codecs. The default value is **FALSE**.

## -remarks

## -see-also
