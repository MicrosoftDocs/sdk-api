---
UID: NF:winuser.GetRawInputBuffer
title: GetRawInputBuffer function (winuser.h)
description: Performs a buffered read of the raw input data.
helpviewer_keywords: ["GetRawInputBuffer","GetRawInputBuffer function [Keyboard and Mouse Input]","_win32_GetRawInputBuffer","_win32_getrawinputbuffer_cpp","inputdev.getrawinputbuffer","winui._win32_getrawinputbuffer","winuser/GetRawInputBuffer"]
old-location: inputdev\getrawinputbuffer.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputbuffer.htm
ms.date: 12/05/2018
ms.keywords: GetRawInputBuffer, GetRawInputBuffer function [Keyboard and Mouse Input], _win32_GetRawInputBuffer, _win32_getrawinputbuffer_cpp, inputdev.getrawinputbuffer, winui._win32_getrawinputbuffer, winuser/GetRawInputBuffer
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetRawInputBuffer
 - winuser/GetRawInputBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetRawInputBuffer
---

# GetRawInputBuffer function

## -description

Performs a buffered read of the raw input messages data found in the calling thread's message queue.

## -parameters

### -param pData [out, optional]

Type: **PRAWINPUT**

A pointer to a buffer of [RAWINPUT](ns-winuser-rawinput.md) structures that contain the raw input data. Pointer should be aligned on a **DWORD** (32-bit) boundary.

If **NULL**, size of the first raw input message data (minimum required buffer), in bytes, is returned in \**pcbSize*.

### -param pcbSize [in, out]

Type: **PUINT**

The size, in bytes, of the provided [RAWINPUT](ns-winuser-rawinput.md) buffer.

### -param cbSizeHeader [in]

Type: **UINT**

The size, in bytes, of the [RAWINPUTHEADER](ns-winuser-rawinputheader.md) structure.

## -returns

Type: **UINT**

If *pData* is **NULL** and the function is successful, the return value is zero. If *pData* is not **NULL** and the function is successful, the return value is the number of [RAWINPUT](ns-winuser-rawinput.md) structures written to *pData*.

If an error occurs, the return value is (**UINT**)-1. Call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the error code.

## -remarks

When an application receives raw input, its message queue gets a [WM_INPUT](/windows/win32/inputdev/wm-input) message and the queue status flag [QS_RAWINPUT](nf-winuser-getqueuestatus.md) is set.

Using **GetRawInputBuffer**, the raw input data is read in the array of variable size [RAWINPUT](ns-winuser-rawinput.md) structures and corresponding [WM_INPUT](/windows/win32/inputdev/wm-input) messages are removed from the calling thread's message queue. You can call this method several times with buffer that cannot fit all message's data until all raw input messages have been read.

The [NEXTRAWINPUTBLOCK](nf-winuser-nextrawinputblock.md) macro allows an application to traverse an array of [RAWINPUT](ns-winuser-rawinput.md) structures.

If all raw input messages have been successfully read from message queue then [QS_RAWINPUT](nf-winuser-getqueuestatus.md) flag is cleared from the calling thread's message queue status.

> [!NOTE]
> WOW64: To get the correct size of the raw input buffer, do not use \**pcbSize*, use \**pcbSize* \* 8 instead. To ensure **GetRawInputBuffer** behaves properly on WOW64, you must align the [RAWINPUT](ns-winuser-rawinput.md) structure by 8 bytes. The following code shows how to align **RAWINPUT** for WOW64.

```csharp
[StructLayout(LayoutKind.Explicit)]
internal struct RAWINPUT
{
    [FieldOffset(0)]
    public RAWINPUTHEADER header;

    [FieldOffset(16+8)]
    public RAWMOUSE mouse;

    [FieldOffset(16+8)]
    public RAWKEYBOARD keyboard;

    [FieldOffset(16+8)]
    public RAWHID hid;
}
```

## -see-also

**Conceptual** 

[GetMessage](nf-winuser-getmessage.md)

[NEXTRAWINPUTBLOCK](nf-winuser-nextrawinputblock.md)

[RAWINPUT](ns-winuser-rawinput.md)

[RAWINPUTHEADER](ns-winuser-rawinputheader.md)

[Raw Input](/windows/win32/inputdev/raw-input)

**Reference**

[Raw Input Overview](/windows/win32/inputdev/about-raw-input)
