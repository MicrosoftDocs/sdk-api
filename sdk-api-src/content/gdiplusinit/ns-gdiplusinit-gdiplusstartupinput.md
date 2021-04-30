---
UID: NS:gdiplusinit.GdiplusStartupInput
title: GdiplusStartupInput
description: The **GdiplusStartupInput** structure holds a block of arguments that are required by the [GdiplusStartup](../gdiplusinit/nf-gdiplusinit-gdiplusstartup.md) function.
helpviewer_keywords: ["GdiplusStartupInput"]
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\gdiplusstartupinput.htm
old-location: gdiplus\_gdiplus_STRUC_GdiplusStartupInput.htm
tech.root: gdiplus
ms.date: 11/4/2019
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: gdiplusinit.h
req.include-header: gdiplus.h
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gdiplusinit.h
api_name:
 - GdiplusStartupInput
f1_keywords:
 - GdiplusStartupInput
 - gdiplusinit/GdiplusStartupInput
dev_langs:
 - c++
---

## -description

The **GdiplusStartupInput** structure holds a block of arguments that are required by the [GdiplusStartup](./nf-gdiplusinit-gdiplusstartup.md) function.

## -struct-fields

### -field GdiplusVersion

Type: **UINT32**

Specifies the version of GDI+. Must be 1.

### -field DebugEventCallback

Type: **[DebugEventProc](./nc-gdiplusinit-debugeventproc.md)**

Pointer to a callback function that GDI+ can call, on debug builds, for assertions and warnings. The default value is **NULL**.

### -field SuppressBackgroundThread

Type: **BOOL**

Boolean value that specifies whether to suppress the GDI+ background thread. If you set this member to **TRUE**, then [GdiplusStartup](/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup) returns (in its *output* parameter) a pointer to a hook function, and a pointer to an unhook function. You must call those functions appropriately to replace the background thread. If you don't want to be responsible for calling the hook and unhook functions, then set this member to **FALSE**. The default value is **FALSE**.

### -field SuppressExternalCodecs

Type: **BOOL**

Boolean value that specifies whether you want GDI+ to suppress external image codecs. GDI+ version 1.0 doesn't support external image codecs, so this field is ignored. The default value is **FALSE**.

## -remarks

The **GdiplusStartupInput** structure provides a constructor that sets the **GdiplusVersion** member to 1, and allows you to specify values for the other three members. All of the constructor parameters are optional, so you can declare a variable of type **GdiplusStartupInput** without passing any arguments to the constructor, and all of the members will be initialized with appropriate default values.

If you set the **SuppressBackgroundThread** member to **TRUE** in the *input* parameter of [GdiplusStartup](./nf-gdiplusinit-gdiplusstartup.md), then you must call the hook and unhook functions returned in the *output* parameter returned by that function. Call those functions before and after the application's main message loop; that is, a message loop that is active for the lifetime of GDI+. Call the hook function before the loop starts, and call the unhook function after the loop ends.

## -see-also

* [GdiplusShutdown]((windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusshutdown)
* [GdiplusStartup](./nf-gdiplusinit-gdiplusstartup.md)
* [GdiplusStartupOutput]((windows/win32/api/gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput)
* [Getting started](/windows/win32/gdiplus/-gdiplus-getting-started-use)