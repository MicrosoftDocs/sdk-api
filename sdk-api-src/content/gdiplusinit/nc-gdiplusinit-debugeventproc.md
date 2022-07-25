---
UID: NC:gdiplusinit.DebugEventProc
title: DebugEventProc
ms.date: 05/07/2020
targetos: Windows
description: \**DebugEventProc** is the signature of a callback function that you implement in your application, and pass to the constructor of [**GdiplusStartupInput**](../gdiplusinit/nf-gdiplusinit-gdiplusstartupinput-gdiplusstartupinput.md).
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
 - LibDef
api_location:
 - gdiplusinit.h
api_name:
 - DebugEventProc
f1_keywords:
 - DebugEventProc
 - gdiplusinit/DebugEventProc
dev_langs:
 - c++
---

## -description

**DebugEventProc** is the signature of a callback function that you implement in your application, and pass to the constructor of [**GdiplusStartupInput**](./nf-gdiplusinit-gdiplusstartupinput-gdiplusstartupinput.md).

## -parameters

### -param level

A [**DebugEventLevel**](./ne-gdiplusinit-debugeventlevel.md) object representing the level of the debug event.

### -param message

A pointer to a narrow string containing the debug event message.

## -remarks

## -see-also
