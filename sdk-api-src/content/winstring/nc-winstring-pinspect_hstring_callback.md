---
UID: NC:winstring.PINSPECT_HSTRING_CALLBACK
title: PINSPECT_HSTRING_CALLBACK (winstring.h)
description: Provides a function pointer to the callback used by the WindowsInspectString function.
helpviewer_keywords: ["PINSPECT_HSTRING_CALLBACK","PINSPECT_HSTRING_CALLBACK function","PINSPECT_HSTRING_CALLBACK function pointer [Windows Runtime]","winrt.pinspect_hstring_callback","winstring/PINSPECT_HSTRING_CALLBACK"]
old-location: winrt\pinspect_hstring_callback.htm
tech.root: WinRT
ms.assetid: B3DAB59B-15A5-42A0-8545-94F585D8FF09
ms.date: 12/05/2018
ms.keywords: PINSPECT_HSTRING_CALLBACK, PINSPECT_HSTRING_CALLBACK function, PINSPECT_HSTRING_CALLBACK function pointer [Windows Runtime], winrt.pinspect_hstring_callback, winstring/PINSPECT_HSTRING_CALLBACK
req.header: winstring.h
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
 - PINSPECT_HSTRING_CALLBACK
 - winstring/PINSPECT_HSTRING_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winstring.h
api_name:
 - PINSPECT_HSTRING_CALLBACK
---

## -description

Provides a function pointer to the callback used by the <a href="/windows/desktop/api/winstring/nf-winstring-windowsinspectstring">WindowsInspectString</a> function.

## -parameters

### -param context

[in]

Custom context data provided to the <a href="/windows/desktop/api/winstring/nf-winstring-windowsinspectstring">WindowsInspectString</a> function.

### -param readAddress

[in]

The address to read data from.

### -param length

[in]

The number of bytes to read, starting at <i>readAddress</i>.

### -param buffer

[out]

The buffer that receives a copy of the bytes that are read.

## -returns

If this function pointer succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implement this callback when you use the <a href="/windows/desktop/api/winstring/nf-winstring-windowsinspectstring">WindowsInspectString</a> function. You can do a cross-process read, read from a dump file, or read from a remote debug debugging session.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowsinspectstring">WindowsInspectString</a>

