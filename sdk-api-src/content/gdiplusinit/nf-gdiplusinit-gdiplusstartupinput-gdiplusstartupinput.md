---
UID: NF:gdiplusinit.GdiplusStartupInput.GdiplusStartupInput
title: GdiplusStartupInput::GdiplusStartupInput
ms.date: 05/07/2020
targetos: Windows
description: Constructor for the [**GdiplusStartupInput**]() structure.
tech.root: gdiplus
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - gdiplusinit.h
api_name:
 - GdiplusStartupInput::GdiplusStartupInput
f1_keywords:
 - GdiplusStartupInput::GdiplusStartupInput
 - gdiplusinit/GdiplusStartupInput::GdiplusStartupInput
dev_langs:
 - c++
---

## -description

Constructor for the [**GdiplusStartupInput**](ns-gdiplusinit-gdiplusstartupinput.md) structure.

The constructor sets the **GdiplusVersion** member to 1. All of the constructor parameters are optional, so you can declare a variable of type **GdiplusStartupInput** without passing any arguments to the constructor, and all of the members will be initialized with appropriate default values.

## -parameters

### -param debugEventCallback

Type: **[DebugEventProc](./nc-gdiplusinit-debugeventproc.md)**

Pointer to your [**DebugEventProc**](./nc-gdiplusinit-debugeventproc.md) callback function, which GDI+ can call on debug builds for assertions and warnings. The default value is **NULL**.

### -param suppressBackgroundThread

Type: **BOOL**

Boolean value that specifies whether to suppress the GDI+ background thread. If you pass **TRUE**, then [**GdiplusStartup**](./nf-gdiplusinit-gdiplusstartup.md) returns (in its *output* parameter) a pointer to a hook function, and a pointer to an unhook function. You must call those functions appropriately to replace the background thread. If you don't want to be responsible for calling the hook and unhook functions, then set this member to **FALSE**. The default value is **FALSE**.

### -param suppressExternalCodecs

Type: **BOOL**

Boolean value that specifies whether you want GDI+ to suppress external image codecs. GDI+ version 1.0 doesn't support external image codecs, so this parameter is ignored. The default value is **FALSE**.

## -remarks

## -see-also
